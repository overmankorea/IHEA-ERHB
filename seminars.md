## Past Seminars

You can find a list of past seminars with a link to the video recording if available.

<style>
  /* 갤러리 전체 컨테이너 */
  .seminar-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 20px; /* 카드 사이 간격 */
    padding: 20px 0;
  }

  /* 개별 카드 스타일 */
  .seminar-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 10px;
    padding: 20px;
    /* 한 줄에 3개씩 배치 (간격 20px 제외하고 계산) */
    flex: 0 1 calc(33.333% - 14px); 
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  /* 마우스 올렸을 때 효과 */
  .seminar-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 15px rgba(0,0,0,0.1);
  }

  /* 내부 텍스트 스타일 */
  .sem-date {
    font-size: 0.85rem;
    color: #666;
    font-weight: 700;
    margin-bottom: 8px;
  }

  .sem-presenter {
    font-size: 0.95rem;
    margin-bottom: 12px;
    line-height: 1.4;
    color: #444;
  }

  .sem-title {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 15px;
    line-height: 1.3;
    color: #2c3e50;
    flex-grow: 1; /* 제목이 짧아도 링크 버튼 위치를 하단으로 통일 */
  }

  .sem-links {
    border-top: 1px solid #eee;
    padding-top: 12px;
    font-size: 0.9rem;
  }

  .sem-links a {
    color: #007bff;
    text-decoration: none;
    font-weight: 600;
  }

  .sem-links a:hover {
    text-decoration: underline;
  }

  /* 반응형: 태블릿 (한 줄에 2개) */
  @media (max-width: 992px) {
    .seminar-card {
      flex: 0 1 calc(50% - 10px);
    }
  }

  /* 반응형: 모바일 (한 줄에 1개) */
  @media (max-width: 600px) {
    .seminar-card {
      flex: 0 1 100%;
    }
  }
</style>

<div class="seminar-grid">
  {% for speaker in site.data.past_seminars %}
    {% if speaker.Video and speaker.Video != "" %}
      <div class="seminar-card">
        <div class="sem-date">Date: {{ speaker.Date }}</div>
      <div class="sem-presenter">
        <strong>Presenter:</strong><br>
        {{ speaker.Presenter }} <span style="color: #888; font-size: 0.85em;">({{ speaker.Institution }})</span>
      </div>
      <div class="sem-title">
        "{{ speaker.Title }}"
      </div>
      <div class="sem-links">
        <strong>Links:</strong>
        <a href="{{ speaker.Video }}" target="_blank">Video Recording</a>
      </div>
    </div>
    {% endif %}
  {% endfor %}
</div>
