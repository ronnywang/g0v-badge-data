list.csv
  - columns: service,name
  - Ex: hackmd,HackMD
  - service: 服務代碼，用在後面的其他設定檔用
  - name: 服務名稱

{service}-id.csv
  - columns: uid,name,sigs
  - uid: 該服務的內部代碼（如果不便公開可以 hash）
  - name: 該服務上的顯示名稱
  - sigs: 單向加密後的一些連結帳號字
    - 統一採用 md5('原字串' . 'g0vg0v') 加密
    - 原字串種類: 
      - email
      - github://{id}
      - facebook://{id}
    - 用 ; 分離

{service}-badge.jsonl
  - columns: uid,time,brief,extra
    - uid: 該服務的內部代碼
    - time: 時間，可以是 2019-04-24 或是 2019-04-24 13:33:00
    - breif: 成就的簡單描述，例如：「使用 emoji 1000 次」
    - extra: 更多其他補充資訊
# g0v-badge-data
