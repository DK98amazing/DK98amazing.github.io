---
layout: post
title: Maven：Maven学习
category: Maven
tags: [Maven]
keywords: Maven
---

## 新版本特性

新版本值得关注的亮点有哪些：

**Maven插件**

	maven copy数据插件
			
		<plugin>
		<groupId>org.apache.maven.plugins</groupId>
		<artifactId>maven-antrun-plugin</artifactId>
		<executions>
		<execution>
		<phase>prepare-package</phase>
		<id>CopyConfigs</id>
		<configuration>
		<target>
		<!-- TODO copy resources to generated ODC environment -->

		<copy todir="${project.build.directory}/assembly/configuration"
		overwrite="true">
		<fileset dir="${basedir}/../runtime-requirement/configuration"
		includes="**" />
		</copy>
		</target>
		</configuration>
		<goals>
		<goal>run</goal>
		</goals>
		</execution>
		</executions>
		</plugin>


	maven 生成可执行jar包插件。
		<plugin>
		<artifactId>maven-assembly-plugin</artifactId>
		<configuration>
		<appendAssemblyId>false</appendAssemblyId>
		<descriptorRefs>
		<descriptorRef>jar-with-dependencies</descriptorRef>
		</descriptorRefs>
		<archive>
		<manifest>
		<!-- 此处指定main方法入口的class -->
		<mainClass>com.utstar.qx.databackup.DataBackUp</mainClass>
		</manifest>
		</archive>
		</configuration>
		<executions>
		<execution>
		<id>make-assembly</id>
		<phase>package</phase>
		<goals>
		<goal>assembly</goal>
		</goals>
		</execution>
		</executions>
		</plugin>

**maven内置变量**

	${basedir} 项目根目录
	${project.build.directory} 构建目录，缺省为target
	${project.build.outputDirectory} 构建过程输出目录，缺省为target/classes
	${project.build.finalName} 产出物名称，缺省为${project.artifactId}-${project.version}
	${project.packaging} 打包类型，缺省为jar
    ${project.xxx} 当前pom文件的任意节点的内容