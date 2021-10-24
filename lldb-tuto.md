# LLDB EASY DEBUG

Add he flag -g3 when you compile your program.

<hr>

Lunch lldb with your executable:

```lldb ./yourprogram ```
<hr>

The target has been created. You can now proceed different

tests by passing arguments with this command in lldb:


```run "your arguments" ```

```fr v``` -> print variable

```print env->t_to_sleep``` -> print variable

```b main``` set a breakpoint in the function

```n``` go forward just one line 
