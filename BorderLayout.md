<h2>BorderLayout佈局管理員</h2>
Container cp = getContentPane(); //取得內容面版

		cp.setLayout(new BorderLayout(10, 10));
		//建立各區域水平、垂直間距為10的BorderLayout物件

		//將各按鈕控制項，加入版面的指定位置
		cp.add(new JButton("EAST"), BorderLayout.EAST);		
		cp.add(new JButton("WEST"), BorderLayout.WEST);
		cp.add(new JButton("SOUTH"), BorderLayout.SOUTH);
		cp.add(new JButton("NORTH"), BorderLayout.NORTH);
		cp.add(new JButton("CENTER"));
