## Schedule

The seminar is held on the **first Monday of each month at 15:30 (UTC)**.

Here is the list of upcoming seminars.

<table width="100%" cellspacing="5" cellpadding="5">
{% for speaker in site.data.past_seminars %}
  {% comment %} 비디오 링크가 비어있거나 존재하지 않을 때만 출력 {% endcomment %}
  {% if speaker.Video == "" or speaker.Video == nil %}
  <tr>
    <td colspan="2" height="40" valign="top" class="session">
      <strong>Date: {{ speaker.Date }}</strong>
    </td>
  </tr>
  
  <tr>
    <td colspan="2" valign="top" class="chair">
      <strong>Presenter:</strong> {{ speaker.Presenter }} ({{ speaker.Institution }})
    </td>
  </tr>
  
  <tr>
    <td colspan="2" valign="top" class="paper">
      <strong>Title:</strong> "{{ speaker.Title }}"
    </td>
  </tr>

  <tr>
    <td colspan="2" height="40" valign="top" class="registration">
      <strong>Links:</strong> <em>Recording not available</em>
    </td>
  </tr>

  <tr style="border-bottom:1px solid #ddd">
    <td colspan="2" style="padding-bottom: 20px;"></td>
  </tr>
  {% endif %}
{% endfor %}
</table>

Join our e-mail list for updates: [https://overmankorea.github.io/IHEA-ERHB/email.html](https://overmankorea.github.io/IHEA-ERHB/email.html).

![Schedule](test.jpg)
