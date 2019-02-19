<h2>載入驅動</h2>
try {//會拋出ClassNotFoundException務必要使用try...catch<br/>
		Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");<br/>
		}catch(Exception ex) {<br/>
			System.out.println("沒有驅動");<br/>
		}
<h2>資料庫連接</h2>
try {//會拋出SQLException務必要使用try...catch
		Connection cn=DriverManager.getConnection("jdbc:sqlserver://127.0.0.1:1433;user=sa;password=nan;database=db_book");<br/>
		System.out.println("資料庫連接成功");<br/>
		}catch(Exception ex) {<br/>
			System.out.println("資料庫連接失敗");<br/>
		}
<h2>取得資料</h2>
		try {
		Connection cn=DriverManager.getConnection("jdbc:sqlserver://127.0.0.1:1433;user=sa;password=nan;database=db_book");<br/>
		System.out.println("資料庫連接成功");<br/>
		Statement sm=cn.createStatement();//使用Connection介面的create Statement()方法取得Statement介面物件<br/>
		ResultSet rs=sm.executeQuery("select top 10 ID from tb_book");//透過Statement介面物件的executeQuery方法執行SELECT語句
		,若要執行INSERT,DELETE,UPDATE則使用executeUpdate("INSERT INTO TABLE_NAME VALUES()")
		<br/>
		ResultSetMetaData rsmd=rs.getMetaData();//取得資料表欄位格式<br/>
		for(int i=1;i<=rsmd.getColumnCount();i++) {<br/>
			System.out.print(rsmd.getCatalogName(i)+"\t");<br/>
		}<br/>
		System.out.println("-----------------------------------------------------");<br/>
		while(rs.next()) {<br/>
			System.out.print(rs.getInt(1)+"\n");<br/>
			}<br/>
			}catch(Exception ex){<br/>
			System.out.println("資料庫操作發生錯誤");
<h2>關閉連線</h2>
		sm.close();
		cn.close();
