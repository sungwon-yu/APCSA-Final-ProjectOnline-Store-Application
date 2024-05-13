# APCSA-Final-ProjectOnline-Store-Application
//Shopping cart Code
import java.util.ArrayList;

public class ShoppingCart {
	
	static ArrayList<Product> shoppingCart = new ArrayList<Product>();
	
	public static void addCart(Product p)
	{
		shoppingCart.add(p);
	}
	
	public static String viewCart()
	{
		Product product;
		String output = " ";
		for(int i = 0; i < shoppingCart.size(); i++)
		{
			product = shoppingCart.get(i);
			output += product.getName() + " " + product.getDescription() + " " + product.getPrice() + " " + product.getQuantity() + " ";
		}
		return output;
	}
	
	public static void modifyCart(Product p, int q)
	{
		for(int i = 0; i < shoppingCart.size(); i++)
		{
			if(p == shoppingCart.get(i))
			{
				shoppingCart.get(i).setQuantity(q);
			}
		}
	}
	
	public static void removeCart(Product p)
	{
		for(int i = 0; i < shoppingCart.size(); i++)
		{
			if(p == shoppingCart.get(i))
			{
				shoppingCart.remove(i);
			}
		}
	}
}
