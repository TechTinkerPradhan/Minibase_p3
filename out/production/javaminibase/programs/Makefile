JDKPATH = /usr
LIBPATH = .:..
CLASSPATH = $(JDKPATH)/lib/classes.zip:.:..:$(LIBPATH)
BINPATH = $(JDKPATH)/bin
JAVAC = $(JDKPATH)/bin/javac -classpath $(CLASSPATH)
JAVA  = $(JDKPATH)/bin/java  -classpath $(CLASSPATH)

BatchInsCompile:BatchInsert.java
	$(JAVAC) BatchInsert.java

BatchInsRun: BatchInsCompile
	$(JAVA) programs.BatchInsert 3125entries.txt minibase_db columnar_file 4

MainCompile:Main.java
	$(JAVAC) Main.java
	$(JAVAC) BatchInsert.java
	$(JAVAC) Query.java

MainRun: MainCompile
	$(JAVA) programs.Main 3125entries.txt minibase_db columnar_file  4