# Markdown入门笔记

## 参考资料

[ 官方cheat-sheet](https://www.markdownguide.org/cheat-sheet/)

pdf精美版cheat-sheet：

{% file src="../.gitbook/assets/markdown-cheatsheet-online.pdf" caption="Markdown CheatSheet" %}

## 清单

<table>
  <thead>
    <tr>
      <th style="text-align:left">Element</th>
      <th style="text-align:left">Markdown Syntax</th>
      <th style="text-align:left">Hot Key in Gitbook</th>
      <th style="text-align:left">Latex</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#x6807;&#x9898;</td>
      <td style="text-align:left">
        <p>#</p>
        <p>##</p>
        <p>###</p>
      </td>
      <td style="text-align:left">
        <p>ctrl+shift+1</p>
        <p>ctrl+shift+2</p>
        <p>null</p>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x52A0;&#x7C97;</td>
      <td style="text-align:left"><code>**blod** or __blod__</code>
      </td>
      <td style="text-align:left">ctrl+b</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x659C;&#x4F53;</td>
      <td style="text-align:left"><code>*italicized* or _italicized_</code>
      </td>
      <td style="text-align:left">ctrl+i</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x5220;&#x9664;&#x7EBF;</td>
      <td style="text-align:left"><code>~~Strikethrough~~</code>
      </td>
      <td style="text-align:left">ctrl+shift+5</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x5F15;&#x7528;&#x5757;</td>
      <td style="text-align:left"><code>&gt; blokquote</code>
      </td>
      <td style="text-align:left">ctrl+]</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x4EE3;&#x7801;&#x5757;</td>
      <td style="text-align:left"><code>`print()`</code>
      </td>
      <td style="text-align:left">ctrl+shift+6</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x56F4;&#x680F;&#x4EE3;&#x7801;&#x5757;</td>
      <td style="text-align:left">
        <p><code>```</code>
        </p>
        <p><code>```</code>
        </p>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">bash&#x56F4;&#x680F;&#x4EE3;&#x7801;&#x5757;</td>
      <td style="text-align:left">
        <p><code>```bash</code>
        </p>
        <p><code>```</code>
        </p>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x6709;&#x5E8F;&#x5217;&#x8868;</td>
      <td style="text-align:left">
        <p><code>1. First item</code>
        </p>
        <p><code>2. Second item</code>
        </p>
      </td>
      <td style="text-align:left">ctrl+shift+7</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x65E0;&#x5E8F;&#x5217;&#x8868;</td>
      <td style="text-align:left"><code>- first item<br />- second item</code>
      </td>
      <td style="text-align:left">ctrl+shift+8</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x4EFB;&#x52A1;&#x5217;&#x8868;</td>
      <td style="text-align:left"><code>- [x] &#x5B66;md<br />- [ ] &#x53D8;&#x597D;&#x770B;</code>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x5206;&#x5272;&#x7EBF;</td>
      <td style="text-align:left"><code>---</code>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x94FE;&#x63A5;</td>
      <td style="text-align:left"><code>[title](url)</code>
      </td>
      <td style="text-align:left">ctrl+k</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x56FE;&#x50CF;</td>
      <td style="text-align:left"><code>![alt text](image.jpg)</code>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x8868;&#x683C;</td>
      <td style="text-align:left">&#x592A;&#x9EBB;&#x70E6;&#x4E0D;&#x60F3;&#x7528;</td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x811A;&#x6CE8;</td>
      <td style="text-align:left">
        <p><code>here&apos;s a footnote<br />[^1]</code>
        </p>
        <p><code>[^1]: This is the footnote.</code>
        </p>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x6570;&#x5B66;&#x516C;&#x5F0F;</td>
      <td style="text-align:left"><code>$$</code>
      </td>
      <td style="text-align:left">null</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>