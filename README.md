# StockJava
# Stock.Java 

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

As you can see from the above file, simple enter in a ticker for an equity and 
you're good to go.  The Data can be accessed in JSON or in a LinkedHashMap<String, String>

One call to the Stock Object generates the JSON: AAPL.getStockJSON();
One call to the Stock Object generates the LinkedHashMap: AAPL.generateStockLinkedHashMap();

Then those structures can be accessed easily using: 

JSONObject apple = AAPL.getStockJSON();

LinkedHashMap<String, String> hash = AAPL.getStockLinkedHashMap();	


