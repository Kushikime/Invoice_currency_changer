When i hit "Create Invoice" button on sale order, odoo open for us a wizard where we can choose some option's.
image 1 to image 2



Then if we hit "Create Invoices" odoo will create an invoice.

The problem here is that, when somebody will check box "Convert to base currency",
the Invoice must take current base currency of the system, in my case it's (USD),
then re-calculate the values for each item, and update invoice with new values.

My plan:
	
1.First try to modify the _create_invoice method of ....class and update the currency to default, if the box is checked.
	
2.When i hit checkbox field that will show 2 variant's of converting:
	a)Use last currency:
		checkbox_first.png
	b)Enter my currency:
		checkbox_second.png
		
In first case system use the currency for the currency which in the Sale Order.
(*the values of currency rate i get from the currency_management)
		
In second case we can enter our currency, and system will use this to calculate new prices of products
		
