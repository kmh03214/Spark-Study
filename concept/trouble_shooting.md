1. spark-submit 명령어 사용시 다음과 같은 에러

error log
~~~zsh
20/09/16 11:08:38 WARN NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.5/bin/jupyter", line 8, in <module>
    sys.exit(main())
  File "/Library/Frameworks/Python.framework/Versions/3.5/lib/python3.5/site-packages/jupyter_core/command.py", line 247, in main
    command = _jupyter_abspath(subcommand)
  File "/Library/Frameworks/Python.framework/Versions/3.5/lib/python3.5/site-packages/jupyter_core/command.py", line 134, in _jupyter_abspath
    'Jupyter command `{}` not found.'.format(jupyter_subcommand)
Exception: Jupyter command `jupyter-/usr/local/Cellar/apache-spark/2.4.6/libexec/conf/pi.py` not found.
log4j:WARN No appenders could be found for logger (org.apache.spark.util.ShutdownHookManager).
log4j:WARN Please initialize the log4j system properly.
log4j:WARN See http://logging.apache.org/log4j/1.2/faq.html#noconfig for more info.
~~~

해결방법
<a href="https://stackoverflow.com/questions/46507887/pyspark-error-executing-jupyter-command-while-running-a-file-using-spark-submit">해결 링크</a>
`$ unset PYSPARK_DRIVER_PYTHON` 입력
