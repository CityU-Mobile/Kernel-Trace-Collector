Kernel-Trace-Collector provides a set of flag in `include/linux/fs.h` to collect traces needed:
```c
...
#define CONFIG_HUBERY_FILETRACER
#ifdef CONFIG_HUBERY_FILETRACER

//#define CONFIG_HUBERY_TRACE_MMAP

//#define CONFIG_HUBERY_TRACE_VFS_OPEN
//#define CONFIG_HUBERY_TRACE_VFS_WRITE
//#define CONFIG_HUBERY_TRACE_VFS_READ

//#define CONFIG_HUBERY_TRACE_READ_PGIDX
//#define CONFIG_HUBERY_TRACE_READAHEAD
//#define CONFIG_HUBERY_CANCEL_READAHEAD

//#define CONFIG_HUBERY_SEQREAD_SIZE

#define CONFIG_HUBERY_TRACE_BIO_READ
//#define CONFIG_HUBERY_TRACE_BIO_WRITE


#define TRACE_CONDITION ((strstr(ss, "com.facebook.katana") != NULL || strstr(ss, "com.twitter.android") != NULL || strstr(ss, "com.facebook.orca") != NULL || strstr(ss, "com.google.earth") != NULL || strstr(ss, "com.threestar.gallery") != NULL || strstr(ss, "com.chrome.dev") != NULL) && (strstr(ss, "apk") != NULL || strstr(ss, "dex") != NULL || strstr(ss, "oat") != NULL || strstr(ss, ".so") != NULL || strstr(ss, "art") != NULL))

#endif
...
```
Users can define the collection conditions, and collect the specific traces by enable flags.
