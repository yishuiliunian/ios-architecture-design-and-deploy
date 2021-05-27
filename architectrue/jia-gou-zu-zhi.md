# 架构组织

### 用户

对于架构而言其用户较多，不止包含最终的终端用户，还包括

* 团队管理者
* 团队中的研发工程师
* 参与工程的其他角色
  * 产品
  * UI/UE

### 交付的产品

主要面向用户交付咨询与工具服务，并分三个层次来交付对应的产品：

* 报告
* 方案
* 工具/服务

报告是对于当前现状的描述，将复杂且难以认知的架构能够被大家以较浅显易懂的方式感知到。同时，根据现状作出一定的判断。包括相对判断和绝对判断，相对判断多是与竞品进行比较得到的比较状态，而绝对判断则是对于一些有绝对标准的事情判断目前我们所处的状态。  


方案是提供奔向一定目标的具体实施路径。包括改进型和激进型。改进型是针对于目前存在一定缺陷的方面进行修补补齐，激进型则是朝着一定的目标进行突击。  


工具/服务 则是我们落地我们的方案的方法，我们提倡能够将方案进行固化。尤其是通过Code将方案固化。  


### 组织构成

主要分成三部分同学：

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x804C;&#x8D23;</th>
      <th style="text-align:left">&#x89E3;&#x91CA;</th>
      <th style="text-align:left">&#x5360;&#x6BD4;</th>
      <th style="text-align:left">&#x6280;&#x672F;&#x6808;&#x53CA;&#x80FD;&#x529B;&#x6A21;&#x578B;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">BP Bussiness Partner</td>
      <td style="text-align:left">&#x5408;&#x4F5C;&#x4F19;&#x4F34;&#x4E0E;&#x4E1A;&#x52A1;&#x65B9;&#x4E00;&#x8D77;&#x5BF9;&#x6700;&#x7EC8;&#x7ED3;&#x679C;&#x8D1F;&#x8D23;&#x3002;&#x540C;&#x65F6;&#xFF0C;&#x4F1A;&#x627F;&#x62C5;&#x90E8;&#x5206;&#x4EA7;&#x54C1;&#x7ECF;&#x7406;&#x7684;&#x89D2;&#x8272;&#x3002;</td>
      <td
      style="text-align:left">20%</td>
        <td style="text-align:left">
          <ul>
            <li>&#x6C9F;&#x901A;&#x80FD;&#x529B;</li>
            <li>&#x9879;&#x76EE;&#x7BA1;&#x7406;&#x80FD;&#x529B;</li>
            <li>&#x7EC4;&#x7EC7;&#x534F;&#x8C03;&#x80FD;&#x529B;</li>
            <li>&#x4EA7;&#x54C1;&#x80FD;&#x529B;</li>
            <li>&#x4E2D;&#x7B49;&#x7AEF;&#x4FA7;&#x77E5;&#x8BC6;</li>
          </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">Engineering</td>
      <td style="text-align:left">&#x5DE5;&#x7A0B;&#x5E08;&#xFF0C;&#x4E3B;&#x8981;&#x8D1F;&#x8D23;&#x5DE5;&#x7A0B;&#x5B9E;&#x73B0;</td>
      <td
      style="text-align:left">70%</td>
        <td style="text-align:left">
          <ul>
            <li>&#x5168;&#x6808;&#x5DE5;&#x7A0B;&#x5E08;
              <ul>
                <li>&#x540E;&#x7AEF;</li>
                <li>&#x524D;&#x7AEF;</li>
              </ul>
            </li>
            <li>&#x7AEF;&#x4FA7;&#x5DE5;&#x7A0B;&#x5E08;
              <ul>
                <li>Android</li>
                <li>iOS</li>
              </ul>
            </li>
          </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">Researcher</td>
      <td style="text-align:left">&#x7814;&#x7A76;&#x8005;&#xFF0C;&#x5BF9;&#x67D0;&#x4E2A;&#x5782;&#x7C7B;&#x95EE;&#x9898;&#x8FDB;&#x884C;&#x6DF1;&#x5165;&#x7814;&#x7A76;&#xFF0C;&#x80FD;&#x591F;&#x5403;&#x900F;&#x67D0;&#x4E2A;&#x5782;&#x7C7B;&#x9886;&#x57DF;&#xFF0C;&#x5E76;&#x63D0;&#x51FA;&#x521B;&#x9020;&#x6027;&#x7684;&#x60F3;&#x6CD5;&#x6216;&#x8005;&#x8BA1;&#x5212;&#x3002;</td>
      <td
      style="text-align:left">10%</td>
        <td style="text-align:left">
          <ul>
            <li>&#x7AEF;&#x4FA7;&#x6280;&#x672F;&#x4E13;&#x5BB6;</li>
          </ul>
        </td>
    </tr>
  </tbody>
</table>

### 价值交付路径

* 从研究中来，到业务中去：Researcher -&gt; Engineering -&gt; BP -&gt; 业务 -&gt; 用户
* 从业务中提炼而来到业务中去：BP -&gt; Engineering -&gt; BP -&gt; 业务 -&gt; 用户

