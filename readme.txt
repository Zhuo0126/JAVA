使用手冊:
1.對專案做Maven install
題目一:
1.批次使用Quartz來做排程，參數調整在com.springboot.demo.config.QuartzConfig(32行)調整執行時間，在執行RunApplication之後，每日18:00會自動排程。
2.DB使用SqlServer，可以在application.properties調整url。
3.由於題目一只要求將每日的美元/台幣欄位(USD/NTD)資料與日期(yyyy-MM-dd HH:mm:ss) insert進DB，而題目二要求卻是需要一次僅查詢一種幣別，鑒於題目要求加入type欄位來精準查詢資料，
所以Create table時除了date和usd欄位之外加入type欄位來判斷幣別。
4.UniTest在test.java.com.springboot.demo.BatchTest，能手動執行指定排程。

題目二:
1.在com.springboot.demo.controller.GameController提供@PostMapping("/forex")，可以使用工具Postman，傳入Json字串，打/forex的url。
2.UniTest在test.java.com.springboot.demo.PostTest，能修改傳入的Request，會返回不同結果。
