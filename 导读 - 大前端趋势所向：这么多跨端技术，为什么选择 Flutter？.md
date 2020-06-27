# 导读 | 大前端趋势所向：这么多跨端技术，为什么选择 Flutter？



## 为什么选择 Flutter ？
节省人力成本，同时不影响用户体验


## 跨端技术的发展过程
<table>
<thead>
<tr>
<th align="left"><strong>技术</strong></th>
<th align="left"><strong>核心</strong></th>
<th align="left"><strong>原生支持</strong></th>
<th align="left"><strong>动态性</strong></th>
<th align="left"><strong>性能</strong></th>
<th align="left"><strong>体验</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Ionic/Cordova</td>
<td align="left">JSBridge 封装给 Web 调用</td>
<td align="left">90%</td>
<td align="left">中</td>
<td align="left">差</td>
<td align="left">差</td>
</tr>
<tr>
<td align="left">React Native/Weex</td>
<td align="left">JIT 模式应用 JS 与原生通信</td>
<td align="left">20%</td>
<td align="left">好</td>
<td align="left">中</td>
<td align="left">中</td>
</tr>
<tr>
<td align="left">Flutter</td>
<td align="left">自渲染</td>
<td align="left">5%</td>
<td align="left">优</td>
<td align="left">良</td>
<td align="left">优</td>
</tr>
</tbody>
</table>

<ul>
<li>Ionic/Cordova（Hybrid），在技术原理上的核心是，将原生的一些能力通过 JSBridge 封装给 Web 来调用，扩充了 Web 应用能力。但是这种方法有两个不足，一是依赖客户端，二是在性能和体验上都非常依赖于 Web 端。因此，整体上的体验不可预知。目前这个技术还经常被应用到，例如，当前 App 内会提供白名单域名和可调用的 JSBridge 方法，由此来增强 H5 与客户端交互能力，从而提升 App 内 H5 的灵活性。</li>
<li>React Native/Weex，在原来的 Hybrid 的 JSBridge 基础上进行改进，将 JavaScript 的界面以及交互转化为 Native 的控件，从而在体验上和原生界面基本一致。但因为是 JIT 模式，因此需要频繁地在 JavaScript 与 Native 之间进行通信，从而会有一定的性能损耗影响，导致体验上与原生会有一些差异。</li>
<li>Flutter，取长补短，结合了之前的一些优点，解决了与 Native 之间通信的问题，同时也有了自渲染模式（框架自身实现了一套 UI 基础框架，与原来的渲染模式基本一致）。从而在体验和性能上相对之前的两种框架表现都较好。
</ul>

## 技术方面：
Hybrid 其实是一个 H5 页面，在每个 APP 中包了一个 H5 的 Web 页面，只是在需要原生功能的地方，通过原生封装一些 JSAPI 给到页面去调用，看起来就像是 H5 拥有了原生 APP 交互功能。所以文章里面说的依赖 Web 的性能就是这个原因。 React Native 以及 Weex ，就改变了用 H5 实现的方式，使用的是原生的界面，但是用户的各类事件操作，都是需要与 JS 进行操作，而 JS 操作后，需要将响应反馈到原生 Native 中，所以需要一个交互过程（ JIT 意思就是运行时编译，就像在运行的时候将 JS 编译为原生界面的过程 ）