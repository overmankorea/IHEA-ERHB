## Schedule

The seminar is held on the **first Monday of each month at 15:30 (UTC)**.

## Upcoming Seminars

Here is the list of upcoming seminars.

<table width="100%" cellspacing="5" cellpadding="5">
  {% assign sorted_seminars = site.data.past_seminars | sort: "Date" %}

  {% for speaker in sorted_seminars %}
    {% if speaker.Video == blank and speaker.Presenter != nil and speaker.Presenter != "" %}
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
    <tr style="border-bottom:1px solid #ddd">
      <td colspan="2" style="padding-bottom: 20px;"></td>
    </tr>
    {% endif %}
  {% endfor %}
</table>

Join our e-mail list for updates: [https://overmankorea.github.io/IHEA-ERHB/email.html](https://overmankorea.github.io/IHEA-ERHB/email.html).

![Schedule](test.jpg)
