# StockJava
Stock.Java 

Description: A Stock Class for Java. Uses the Yahoo Finance API
--------------------------------------------------------------------------------
Test File:

	import java.io.IOException;
	import org.json.simple.JSONObject;
	import java.util.*;


	public class StockTest {

	public static void main(String[] args)  throws java.net.MalformedURLException, IOException{
		Stock AAPL = new Stock("AAPL");
		AAPL.generateStockJSON();
		JSONObject apple = AAPL.getStockJSON();
		AAPL.generateStockLinkedHashMap();
		LinkedHashMap<String, String> hash = AAPL.getStockLinkedHashMap();
		
		System.out.println(apple);
		System.out.println(hash);
		

	}

	}

----------------------------------------------------------------------------------


