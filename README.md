<h2 style="word-wrap: break-word;margin-top: 24px;margin-bottom: 16px;padding-bottom: 0.3em;font-size: 1.5em;line-height: 1.25;box-sizing: border-box;font-weight: 600;border-bottom: 1px solid rgb(234, 236, 239);color: rgb(36, 41, 46);white-space: normal;background-color: rgb(255, 255, 255);"><span style="font-size: 17px;">0x0 介绍</span></h2><p style="word-wrap: break-word;margin-bottom: 16px;line-height: normal;box-sizing: border-box;color: rgb(36, 41, 46);text-align: left;white-space: normal;background-color: rgb(255, 255, 255);">Burp Suite 是用于攻击web 应用程序的集成平台，包含了许多神器。Burp Suite为这些工具设计了许多接口，以加快攻击应用程序的过程。所有工具都共享一个请求，并能处理对应的HTTP 消息、持久性、认证、代理、日志、警报。为什么要汉化？做为一个半路出家英语不好的人时常不认识某些单词而烦恼，现在终于由<span style="color: rgb(51, 51, 51);font-family: -apple-system-font, BlinkMacSystemFont, &quot;Helvetica Neue&quot;, &quot;PingFang SC&quot;, &quot;Hiragino Sans GB&quot;, &quot;Microsoft YaHei UI&quot;, &quot;Microsoft YaHei&quot;, Arial, sans-serif;font-size: 17px;text-align: justify;">凌天安全实验室的小伙伴汉化了这个渗透测试中的“大杀器”！</span></p><h2 style="word-wrap: break-word;margin-top: 24px;margin-bottom: 16px;padding-bottom: 0.3em;font-size: 1.5em;line-height: 1.25;box-sizing: border-box;font-weight: 600;border-bottom: 1px solid rgb(234, 236, 239);color: rgb(36, 41, 46);white-space: normal;background-color: rgb(255, 255, 255);"><span style="font-size: 17px;">0x1 使用方法</span></h2><p style="word-wrap: break-word;margin-bottom: 16px;line-height: normal;box-sizing: border-box;color: rgb(36, 41, 46);text-align: left;white-space: normal;background-color: rgb(255, 255, 255);">早期我司大牛就已经提出来，javaagent技术，该技术应用很广这里是是小试牛刀，JavaAgent 是运行在 main方法之前的拦截器，它内定的方法名叫 premain ，也就是说先执行 premain 方法然后再执行 main 方法。用处都明白了吧。具体代码可以反编译jar包。 这里只是用提前翻译好的文本替换了burp内的字节码内容。按道理所有burp都能使用本工具，但是我只测试1.7.X～2.X的版本防止有部分人爱钻牛角尖，所以你懂得。欢迎各路大佬测试是否有后门。</p><h3 style="word-wrap: break-word;margin-top: 24px;margin-bottom: 16px;font-size: 1.25em;line-height: 1.25;box-sizing: border-box;background: rgb(255, 255, 255);border-top: 3px solid rgb(153, 153, 153);font-weight: 600;color: rgb(36, 41, 46);white-space: normal;padding-left: 15px !important;"><span style="font-size: 17px;">Linux Mac 下加载 burp-loader-keygen.jar</span></h3><pre style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(36, 41, 46);font-size: 16px;text-align: left;background-color: rgb(255, 255, 255);"><code class="hljs nginx" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;display: block;overflow-x: auto;padding: 0.5em;white-space: pre-wrap;background: rgb(35, 36, 31) !important;color: rgb(248, 248, 242) !important;"><span class="hljs-attribute" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(102, 217, 239);">java</span> -javaagent:BurpSuiteCn.jar -Xbootclasspath/p:burp-loader-keygen.jar &nbsp;-Xmx1024m -jar burpsuite_pro_v1.x.x.jar</code></pre><h3 style="word-wrap: break-word;margin-top: 24px;margin-bottom: 16px;font-size: 1.25em;line-height: 1.25;box-sizing: border-box;background: rgb(255, 255, 255);border-top: 3px solid rgb(153, 153, 153);font-weight: 600;color: rgb(36, 41, 46);white-space: normal;padding-left: 15px !important;"><span style="font-size: 17px;">Windwos 下加载 burp-loader-keygen.jar</span></h3><blockquote style="word-wrap: break-word;line-height: normal;box-sizing: border-box;margin-bottom: 16px;padding-right: 1em;padding-left: 1em;color: rgb(106, 115, 125);border-left-width: 0.25em;border-left-color: rgb(223, 226, 229);text-align: left;white-space: normal;background-color: rgb(255, 255, 255);"><p style="word-wrap: break-word;line-height: normal;box-sizing: border-box;">需要指定编码否则会乱码！！！</p></blockquote><pre style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(36, 41, 46);font-size: 16px;text-align: left;background-color: rgb(255, 255, 255);"><code class="hljs nginx" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;display: block;overflow-x: auto;padding: 0.5em;white-space: pre-wrap;background: rgb(35, 36, 31) !important;color: rgb(248, 248, 242) !important;"><span class="hljs-attribute" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(102, 217, 239);">java</span> -Dfile.encoding=utf-<span class="hljs-number" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(174, 129, 255);">8</span> -javaagent:BurpSuiteCn.jar -Xbootclasspath/p:burp-loader-keygen.jar &nbsp;-Xmx1024m -jar burpsuite_pro_v1.x.x.jar</code></pre><h3 style="word-wrap: break-word;margin-top: 24px;margin-bottom: 16px;font-size: 1.25em;line-height: 1.25;box-sizing: border-box;background: rgb(255, 255, 255);border-top: 3px solid rgb(153, 153, 153);font-weight: 600;color: rgb(36, 41, 46);white-space: normal;padding-left: 15px !important;"><span style="font-size: 17px;">自定义翻译规则</span></h3><blockquote style="word-wrap: break-word;line-height: normal;box-sizing: border-box;margin-bottom: 16px;padding-right: 1em;padding-left: 1em;color: rgb(106, 115, 125);border-left-width: 0.25em;border-left-color: rgb(223, 226, 229);text-align: left;white-space: normal;background-color: rgb(255, 255, 255);"><p style="word-wrap: break-word;line-height: normal;box-sizing: border-box;">包内自带翻译包。 在同目录下新建cn.txt写入一下内容如： 注意一下 \t 是分割符， 左边是需要匹配的 右边是替换的 支持正则表达式。</p></blockquote><pre style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(36, 41, 46);font-size: 16px;text-align: left;background-color: rgb(255, 255, 255);"><code class="hljs nginx" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;display: block;overflow-x: auto;padding: 0.5em;white-space: pre-wrap;background: rgb(35, 36, 31) !important;color: rgb(248, 248, 242) !important;"><span class="hljs-attribute" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(102, 217, 239);">Proxy</span> \t 代理 
The analysis is based <span class="hljs-literal" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(174, 129, 255);">on</span> a sample of ([<span class="hljs-number" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(174, 129, 255);">0</span>-<span class="hljs-number" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(174, 129, 255);">9</span>]+) tokens?. Based <span class="hljs-literal" style="word-wrap: break-word;line-height: normal;box-sizing: border-box;color: rgb(174, 129, 255);">on</span> the sample size, the reliability of the results is: (.*) <span style="font-size: 18px;"><strong style="font-size: 18px;white-space: normal;">
