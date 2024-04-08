# Contributing to translations

{% hint style="warning" %}
Follow the linked guide first to set up the project.
{% endhint %}

{% content-ref url="build-guide/" %}
[build-guide](build-guide/)
{% endcontent-ref %}

***

{% hint style="danger" %}
Be sure to create the new file while using(checked out) the DEV branch, not MASTER.
{% endhint %}

Duplicate the en.json and adjust its file name according to the wanted language code, e.g. da.json (Danish)

{% embed url="https://github.com/tiltedphoques/TiltedEvolution/blob/master/Code/skyrim_ui/src/assets/i18n/en.json" %}

{% hint style="info" %}
You can find the language codes on this page or by using google e.g. "danish language code"

[http://www.lingoes.net/en/translator/langcode.htm](http://www.lingoes.net/en/translator/langcode.htm)
{% endhint %}

Then translate all strings in the file.

{% hint style="danger" %}
Do not change the key words such as the underline and similar coloured in green. ![](../.gitbook/assets/image.png)
{% endhint %}

Then create a pull request like [https://github.com/tiltedphoques/TiltedEvolution/pull/573](https://github.com/tiltedphoques/TiltedEvolution/pull/573) with your new localisation file.

