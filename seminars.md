## Past Seminars

You can find a list of past seminars with a link to the video recording if available.

<table width="100%" cellspacing="5" cellpadding="5">
{% for speaker in site.data.past_seminars %}
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
      {% if speaker.Video and speaker.Video != "" %}
        <strong>Links:</strong> <a href="{{ speaker.Video }}" target="_blank">Video Recording</a>
      {% else %}
        <strong>Links:</strong> <em>Recording not available</em>
      {% endif %}
    </td>
  </tr>

  <tr style="border-bottom:1px solid #ddd">
    <td colspan="2" style="padding-bottom: 20px;"></td>
  </tr>
{% endfor %}
</table>
