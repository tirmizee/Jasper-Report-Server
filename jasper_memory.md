
##### การตั้งค่า heap memory ใน jasper server

- ##### แก้ไขไฟล์ apache-tomcat/bin/setenv.sh

      # Load Tomcat Native Library
      LD_LIBRARY_PATH=/opt/jasperreports-server-cp-7.8.0/common/lib:$LD_LIBRARY_PATH

      JAVA_HOME=/opt/jasperreports-server-cp-7.8.0/java
      JRE_HOME=$JAVA_HOME
      JAVA_OPTS="-Djs.license.directory=/opt/jasperreports-server-cp-7.8.0 $JAVA_OPTS "
      JAVA_OPTS=" $JAVA_OPTS "
      JAVA_OPTS="-Xms1024m -Xmx2048m -Xss2m $JAVA_OPTS " # java-memory-settings
      export JAVA_HOME
      export JRE_HOME
      export JAVA_OPTS
      export LD_LIBRARY_PATH
			    
- #####  run ./catalina.sh เพื่อเริ่มต้น tomcat ใหม่
