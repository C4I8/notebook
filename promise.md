# Promise<br>
## 同步与异步<br>
同步是指:当程序1调用程序2时,程序1停下不动,直到程序2完成回到程序1来,程序1才继续执行下去.<br>
异步是指:当程序1调用程序2时,程序1径自继续自己的下一个动作,不受程序2的的影响.<br>
<hr>
同步是指:发送方发出数据后,等接收方发回响应以后才发下一个数据包的通讯方式.<br>
异步是指:发送方发出数据后,不等接收方发回响应,接着发送下个数据包的通讯方式.<br>
<hr>
一个异步的例子<br>

      function a(callback){
          console.log("aaaa");
          setTimeout(callback,0);
      }

      function b(){
          console.log("bbbb");
      }

      function callback(){
          console.log("callback");
      }

      function fnc(){
            a(callback);
            b();
      }

      fnc();
      //顺序输出
      //aaaa
      //bbbb
      //callback
如上所示,fnc函数执行过程中,先调用了a函数,再径直调用b函数,不受a函数的影响.<br>
JavaScript中回调函数是异步的基础形式,但不是优秀的解决方案.<br>
## Promise异步方案
