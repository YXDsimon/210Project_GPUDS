# 210Project_GDS

## Overview guide

For direct data transfers between GPU memory and storage, the file must be opened in O_DIRECT mode.

　

```c++
//常规打开文件，需要通过CPU拷贝
int fd = open(file_name,...)
void *sysmem_buf, *gpumem_buf;
sysmem_buf = malloc(buf_size);
cudaMalloc(gpumem_buf, buf_size);
pread(fd, sysmem_buf, buf_size);
cudaMemcpy(sysmem_buf, 
  gpumem_buf, buf_size, H2D); 
doit<<<gpumem_buf, …>>> 
// no faults; 
```

```
//GDS 使用mmap（是什么？）打开文件，跳过CPU
int fd = open(file_name, O_DIRECT,...)
void *mgd_mem_buf;
cudaMallocManaged(mgd_mem_buf, buf_size);
mmap(mgd_mem_buf, buf_size, …, fd, …)
doit<<<mgd_mem_buf, …>>> 
```

