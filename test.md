# SIGNALL FOR APPLICATION

�°���źź�������װ�ɾɰ汾�Ľӿڡ�
```c
int sigall(int signo, void *(*CallBack)(int))
{
  struct sigaction act, oact;
  act.sa_handler = CallBack;
  sigemptyset(&act.samask);
  act.sa_flags = 0;
  return sigaction(signo, &act, &oact);
}
```
