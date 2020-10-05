# Restaurant
Restaurant Java Eclipse 
package Restaurant_S;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.LineBorder;
import java.awt.Color;
import javax.swing.JLabel;
import java.awt.Font;
import javax.swing.JTextField;
import javax.swing.JTabbedPane;
import javax.swing.JButton;
import javax.swing.JComboBox;
import javax.swing.DefaultComboBoxModel;
import javax.swing.JCheckBox;
import javax.swing.JSeparator;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;

public class Restaurants {

	private JFrame frame;
	private JTextField jtxChickenBurger;
	private JTextField jtxBurgerMeal;
	private JTextField jtxBCBurger;
	private JTextField textField_3;
	private JTextField textField_4;
	private JTextField jtxQty;
	private JTextField jtxConver;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Restaurants window = new Restaurants();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Restaurants() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.setBounds(0, 0, 1368, 689);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JPanel panel = new JPanel();
		panel.setBorder(new LineBorder(new Color(0, 0, 0), 6));
		panel.setBounds(64, 133, 499, 230);
		frame.getContentPane().add(panel);
		panel.setLayout(null);
		
		JLabel lblNewLabel_1 = new JLabel("Chicken Burger");
		lblNewLabel_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1.setBounds(25, 13, 136, 16);
		panel.add(lblNewLabel_1);
		
		JLabel lblNewLabel_1_1 = new JLabel("Chicken Burger Meal");
		lblNewLabel_1_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_1.setBounds(25, 65, 180, 16);
		panel.add(lblNewLabel_1_1);
		
		JLabel lblNewLabel_1_2 = new JLabel("Cheese Burgher");
		lblNewLabel_1_2.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_2.setBounds(25, 111, 136, 16);
		panel.add(lblNewLabel_1_2);
		
		jtxChickenBurger = new JTextField();
		jtxChickenBurger.setFont(new Font("Tahoma", Font.PLAIN, 18));
		jtxChickenBurger.setBounds(301, 12, 162, 28);
		panel.add(jtxChickenBurger);
		jtxChickenBurger.setColumns(10);
		
		jtxBurgerMeal = new JTextField();
		jtxBurgerMeal.setFont(new Font("Tahoma", Font.PLAIN, 18));
		jtxBurgerMeal.setColumns(10);
		jtxBurgerMeal.setBounds(301, 64, 162, 28);
		panel.add(jtxBurgerMeal);
		
		jtxBCBurger = new JTextField();
		jtxBCBurger.setFont(new Font("Tahoma", Font.PLAIN, 18));
		jtxBCBurger.setColumns(10);
		jtxBCBurger.setBounds(301, 105, 162, 28);
		panel.add(jtxBCBurger);
		
		final JComboBox jCmbDrink = new JComboBox();
		jCmbDrink.setModel(new DefaultComboBoxModel(new String[] {"Select a drink", "Apple juice", "Tea ", "Ice Tea", "Cola", "Coke", "Coffe", "Ice Coffe ", "Orange", ""}));
		jCmbDrink.setBounds(25, 154, 122, 22);
		panel.add(jCmbDrink);
		
		jtxQty = new JTextField();
		jtxQty.setFont(new Font("Tahoma", Font.PLAIN, 18));
		jtxQty.setColumns(10);
		jtxQty.setBounds(301, 165, 162, 28);
		panel.add(jtxQty);
		
		JLabel lblNewLabel_1_2_2 = new JLabel("Qty");
		lblNewLabel_1_2_2.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_2_2.setBounds(301, 145, 136, 16);
		panel.add(lblNewLabel_1_2_2);
		
		final JCheckBox jCTax = new JCheckBox("Tax");
		jCTax.setBounds(299, 196, 113, 25);
		panel.add(jCTax);
		
		final JCheckBox jCDelivery = new JCheckBox("Home Delivery\r\n");
		jCDelivery.setBounds(25, 185, 113, 25);
		panel.add(jCDelivery);
		
		JSeparator separator = new JSeparator();
		separator.setBounds(12, 140, 480, 6);
		panel.add(separator);
		
		JPanel panel_1 = new JPanel();
		panel_1.setBorder(new LineBorder(new Color(0, 0, 0), 6));
		panel_1.setBounds(600, 133, 230, 230);
		frame.getContentPane().add(panel_1);
		panel_1.setLayout(null);
		
	
		final JComboBox jcmbCurrency = new JComboBox();
		jcmbCurrency.setModel(new DefaultComboBoxModel(new String[] {"Chose One", "USA", "Nigeria", "Romania", "Argentina", "Germania", "Brazilia", "Japonia"}));
		jcmbCurrency.setBounds(38, 26, 162, 22);
		panel_1.add(jcmbCurrency);
		
		jtxConver = new JTextField();
		jtxConver.setBounds(38, 61, 162, 37);
		jtxConver.setFont(new Font("Tahoma", Font.PLAIN, 18));
		jtxConver.setColumns(10);
		panel_1.add(jtxConver);
		
		JLabel lblNewLabel_2_4 = new JLabel("");
		lblNewLabel_2_4.setFont(new Font("Tahoma", Font.BOLD, 18));
		lblNewLabel_2_4.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		lblNewLabel_2_4.setBounds(38, 111, 162, 37);
		panel_1.add(lblNewLabel_2_4);
		
		JButton JbtnConvert = new JButton("Convert");
		JbtnConvert.setBounds(12, 169, 97, 25);
		panel_1.add(JbtnConvert);
		
		JButton JbtnClose = new JButton("Close");
		JbtnClose.setBounds(121, 169, 97, 25);
		panel_1.add(JbtnClose);
		
		JPanel panel_2 = new JPanel();
		panel_2.setBorder(new LineBorder(new Color(0, 0, 0), 6));
		panel_2.setBounds(64, 376, 499, 168);
		frame.getContentPane().add(panel_2);
		panel_2.setLayout(null);
		
		final JLabel lblNewLabel_1_3 = new JLabel("Cost Of Drinks");
		lblNewLabel_1_3.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_3.setBounds(12, 24, 136, 16);
		panel_2.add(lblNewLabel_1_3);
		
		final JLabel lblNewLabel_1_1_1 = new JLabel("Cost Of Meal");
		lblNewLabel_1_1_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_1_1.setBounds(12, 76, 180, 16);
		panel_2.add(lblNewLabel_1_1_1);
		
		final JLabel lblNewLabel_1_2_1 = new JLabel("Cost of Delivery");
		lblNewLabel_1_2_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_2_1.setBounds(12, 122, 136, 16);
		panel_2.add(lblNewLabel_1_2_1);
		
		final JLabel jlblCostOfDrinks = new JLabel("");
		jlblCostOfDrinks.setFont(new Font("Tahoma", Font.BOLD, 18));
		jlblCostOfDrinks.setBounds(254, 24, 187, 31);
		jlblCostOfDrinks.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		panel_2.add(jlblCostOfDrinks);
		
		final JLabel jlblCostMeal = new JLabel("");
		jlblCostMeal.setFont(new Font("Tahoma", Font.BOLD, 18));
		jlblCostMeal.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		jlblCostMeal.setBounds(254, 76, 187, 31);
		panel_2.add(jlblCostMeal);
		
		final JLabel jlblCostOfDelivery = new JLabel("");
		jlblCostOfDelivery.setFont(new Font("Tahoma", Font.BOLD, 18));
		jlblCostOfDelivery.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		jlblCostOfDelivery.setBounds(254, 122, 187, 31);
		panel_2.add(jlblCostOfDelivery);
		
		JPanel panel_1_1 = new JPanel();
		panel_1_1.setBorder(new LineBorder(new Color(0, 0, 0), 6));
		panel_1_1.setBounds(575, 376, 279, 168);
		frame.getContentPane().add(panel_1_1);
		panel_1_1.setLayout(null);
		
		JLabel lblNewLabel_1_3_1 = new JLabel("Tax");
		lblNewLabel_1_3_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_3_1.setBounds(12, 13, 136, 16);
		panel_1_1.add(lblNewLabel_1_3_1);
		
		JLabel lblNewLabel_1_1_1_1 = new JLabel("Sub Total");
		lblNewLabel_1_1_1_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_1_1_1.setBounds(12, 65, 180, 16);
		panel_1_1.add(lblNewLabel_1_1_1_1);
		
		JLabel lblNewLabel_1_2_1_1 = new JLabel("Total");
		lblNewLabel_1_2_1_1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		lblNewLabel_1_2_1_1.setBounds(12, 111, 136, 16);
		panel_1_1.add(lblNewLabel_1_2_1_1);
		
		final JLabel jljblTax = new JLabel("");
		jljblTax.setFont(new Font("Tahoma", Font.BOLD, 18));
		jljblTax.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		jljblTax.setBounds(180, 13, 87, 31);
		panel_1_1.add(jljblTax);
		
		final JLabel jlblSubTotal = new JLabel("");
		jlblSubTotal.setFont(new Font("Tahoma", Font.BOLD, 18));
		jlblSubTotal.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		jlblSubTotal.setBounds(180, 65, 87, 31);
		panel_1_1.add(jlblSubTotal);
		
		final JLabel jlblTotal = new JLabel("");
		jlblTotal.setFont(new Font("Tahoma", Font.BOLD, 18));
		jlblTotal.setBorder(new LineBorder(new Color(0, 0, 0), 2));
		jlblTotal.setBounds(180, 111, 87, 31);
		panel_1_1.add(jlblTotal);
		
		JPanel panel_1_2 = new JPanel();
		panel_1_2.setBorder(new LineBorder(new Color(0, 0, 0), 6));
		panel_1_2.setBounds(856, 132, 299, 392);
		frame.getContentPane().add(panel_1_2);
		panel_1_2.setLayout(null);
		
		JTabbedPane tabbedPane = new JTabbedPane(JTabbedPane.TOP);
		tabbedPane.setBounds(12, 34, 275, 345);
		panel_1_2.add(tabbedPane);
		
		JPanel panel_3 = new JPanel();
		tabbedPane.addTab("Receipt", null, panel_3, null);
		panel_3.setLayout(null);
		
		textField_4 = new JTextField();
		textField_4.setBounds(12, 13, 246, 302);
		panel_3.add(textField_4);
		textField_4.setColumns(10);
		
		JPanel panel_4 = new JPanel();
		tabbedPane.addTab("Calculator", null, panel_4, null);
		panel_4.setLayout(null);
		
		JButton btnBackSpace = new JButton("<-");
		btnBackSpace.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnBackSpace.setBounds(12, 63, 63, 50);
		panel_4.add(btnBackSpace);
		
		JButton btnClear = new JButton("C");
		btnClear.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnClear.setBounds(74, 63, 50, 50);
		panel_4.add(btnClear);
		
		JButton btnPrecent = new JButton("%");
		btnPrecent.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnPrecent.setBounds(121, 63, 63, 50);
		panel_4.add(btnPrecent);
		
		textField_3 = new JTextField();
		textField_3.setColumns(10);
		textField_3.setBounds(12, 13, 243, 51);
		panel_4.add(textField_3);
		
		JButton btn8 = new JButton("8");
		btn8.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn8.setBounds(12, 109, 50, 50);
		panel_4.add(btn8);
		
		JButton btn9 = new JButton("9");
		btn9.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn9.setBounds(59, 109, 50, 50);
		panel_4.add(btn9);
		
		JButton btnDiv = new JButton("/");
		btnDiv.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnDiv.setBounds(108, 109, 50, 50);
		panel_4.add(btnDiv);
		
		JButton btnMult = new JButton("*");
		btnMult.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnMult.setBounds(157, 109, 50, 50);
		panel_4.add(btnMult);
		
		JButton btnPLUS = new JButton("+");
		btnPLUS.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnPLUS.setBounds(205, 109, 50, 50);
		panel_4.add(btnPLUS);
		
		JButton btnSub = new JButton("-");
		btnSub.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnSub.setBounds(205, 156, 50, 50);
		panel_4.add(btnSub);
		
		JButton btn7 = new JButton("7");
		btn7.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn7.setBounds(157, 156, 50, 50);
		panel_4.add(btn7);
		
		JButton btn6 = new JButton("6");
		btn6.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn6.setBounds(108, 156, 50, 50);
		panel_4.add(btn6);
		
		JButton btn5 = new JButton("5");
		btn5.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn5.setBounds(59, 156, 50, 50);
		panel_4.add(btn5);
		
		JButton btn4 = new JButton("4");
		btn4.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn4.setBounds(12, 156, 50, 50);
		panel_4.add(btn4);
		
		JButton btn3 = new JButton("3");
		btn3.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn3.setBounds(12, 204, 50, 50);
		panel_4.add(btn3);
		
		JButton btn2 = new JButton("2");
		btn2.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn2.setBounds(59, 204, 50, 50);
		panel_4.add(btn2);
		
		JButton btn1 = new JButton("1");
		btn1.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn1.setBounds(108, 204, 50, 50);
		panel_4.add(btn1);
		
		JButton btn0 = new JButton("0");
		btn0.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btn0.setBounds(157, 204, 50, 50);
		panel_4.add(btn0);
		
		JButton btnEqual = new JButton("=");
		btnEqual.setFont(new Font("Tahoma", Font.PLAIN, 18));
		btnEqual.setBounds(205, 204, 50, 50);
		panel_4.add(btnEqual);
		
		JPanel panel_2_1 = new JPanel();
		panel_2_1.setBorder(new LineBorder(new Color(0, 0, 0), 6));
		panel_2_1.setBounds(64, 568, 1091, 74);
		frame.getContentPane().add(panel_2_1);
		panel_2_1.setLayout(null);
		
		JButton JbtnTotal = new JButton("Total");
		JbtnTotal.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				
				
				
				 double ChicBurger = Double.parseDouble(jtxBCBurger.getText());
				 double ChicBurgerPrice= 2.39;
				 double Burger;
				Burger = (ChicBurger * ChicBurgerPrice);
				String pMeal = String.format("%.2f", Burger);
				jlblCostMeal.setText(pMeal);
				
				
				 double ChicBurgerMeal = Double.parseDouble(jtxBurgerMeal.getText());
				 double ChicBurgerMealPrice= 4.39;
				 double BurgerMeal;
				BurgerMeal = (ChicBurgerMeal * ChicBurgerMealPrice);
				String cbMeal = String.format("%.2f", BurgerMeal + Burger);
				jlblCostMeal.setText(cbMeal);
				
				
				 double CheeseBurger = Double.parseDouble(jtxChickenBurger.getName());
				 double CheeseBurgerPrice= 3.39;
				 double CheeseBurgerMeal;
				CheeseBurgerMeal = (CheeseBurger * CheeseBurgerPrice);
				String cheese = String.format("%.2f", CheeseBurgerMeal + BurgerMeal + Burger);
				jlblCostMeal.setText(cheese);
//------------------------------------------------------------Delivery-----------------------------------------------------------------------------------------------------------------
		
			
				double iDelivery = 3.39;
				if(jCDelivery.isSelected())
				{
					String pDelivery = String.format("%2.f",  iDelivery);
					jlblCostOfDelivery.setText(pDelivery);
				}
				else {
					jlblCostOfDelivery.setText("0");
				}
				
			

			//----------------------------------------------------Drinks-----------------------------------------------------------------------------------------------------------------
			
			double Drinks = Double.parseDouble(jtxQty.getText());
			double Tea=1.20 * Drinks;
			double Ice_Tea=0.90 * Drinks;
			double Coffee=2.50 * Drinks;
			double Ice_Coffee=1.10 * Drinks;
			double Cola=2.10 * Drinks;
			double Coke=1.60 * Drinks;
			double Orange=1.70 * Drinks;
			double Apple_juice=1.70 * Drinks;

			
			if(jCmbDrink.getSelectedItem().equals("Aplle juice"))
			{
				String cApple_Juice = String.format("%.2f", Apple_juice);
				jlblCostOfDrinks.setText(cApple_Juice);
			}
			if(jCmbDrink.getSelectedItem().equals("Tea"))
			{
				String cTea_Juice = String.format("%.2f", Tea);
				jlblCostOfDrinks.setText(cTea_Juice);
			}
			if(jCmbDrink.getSelectedItem().equals("Ice Tea"))
			{
				String cIce_Tea = String.format("%.2f", Ice_Tea);
				jlblCostOfDrinks.setText(cIce_Tea);
			}
			if(jCmbDrink.getSelectedItem().equals("Coke"))
			{
				String cCoke = String.format("%.2f", Coke);
				jlblCostOfDrinks.setText(cCoke);
			}
			if(jCmbDrink.getSelectedItem().equals("Cola"))
			{
				String cCola = String.format("%.2f", Cola);
				jlblCostOfDrinks.setText(cCola);
			}
			if(jCmbDrink.getSelectedItem().equals("Orange"))
			{
				String cOrange = String.format("%.2f", Orange);
				jlblCostOfDrinks.setText(cOrange);
			}
			if(jCmbDrink.getSelectedItem().equals("Coffee"))
			{
				String cCoffee = String.format("%.2f", Coffee);
				jlblCostOfDrinks.setText(cCoffee);
			}
			if(jCmbDrink.getSelectedItem().equals("Ice Coffee"));
			{
				String cIceCoffee = String.format("%.2f", Ice_Coffee);
				jlblCostOfDrinks.setText(cIceCoffee);
			}
			if(jCmbDrink.getSelectedItem().equals("Select a drink"))
			{
				jlblCostOfDrinks.setText("0");
			}
			
//----------------------------------------------------------------- Tax Rate -------------------------------------------------------------------------------------------------------------------------------------------------------------------------
			double cTotal1 = Double.parseDouble(jlblCostOfDrinks.getText());
			double cTotal2 = Double.parseDouble(jlblCostMeal.getText());
			double cTotal3 = Double.parseDouble(jlblCostOfDelivery.getText());
			double AllTotal = (cTotal1 + cTotal2 + cTotal3)/100;
			if(jCTax.isSelected())
			{
				String iTotal = String.format("%.2f", AllTotal);
				jljblTax.setText(iTotal);
			}
			
//----------------------------------------------------------------Total----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
			double cTotal4 = Double.parseDouble(jljblTax.getText());
			
			double subTotal = (cTotal1 + cTotal2 + cTotal3);
			String isubTotal = String.format("$ %2.f", subTotal);
			jlblSubTotal.setText(isubTotal);
			
			double allTotal = (cTotal1 + cTotal2 + cTotal3);
			String iTotal = String.format("$ %2.f", allTotal);
			jlblTotal.setText(iTotal);
			
			String iTaxTotal = String.format("$ %2.f", cTotal4);
			jljblTax.setText(iTaxTotal);
			
			
			
			
			}
			});
		JbtnTotal.setBounds(163, 24, 97, 25);
		panel_2_1.add(JbtnTotal);
		
		JButton JbtnReceipt = new JButton("Receipt");
		JbtnReceipt.setBounds(393, 24, 97, 25);
		panel_2_1.add(JbtnReceipt);
		
		JButton JbtnReset = new JButton("Reset");
		JbtnReset.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				jlblCostOfDelivery.setText(null);
				
				jlblSubTotal.setText(null);
				jlblTotal.setText(null);
				jljblTax.setText(null);
				jtxConver.setText(null);
				jlblCostOfDelivery.setText(null);
				jlblCostOfDrinks.setText(null);
				jlblCostMeal.setText(null);
				jlblCostOfDelivery.setText(null);
				jlblSubTotal.setText(null);
				jlblTotal.setText(null);
				jljblTax.setText(null);
				jtxBCBurger.setText(null);
				jtxBurgerMeal.setText(null);
				jtxChickenBurger.setText(null);
				jtxQty.setText(null);
				jtxConver.setText(null);
				jCmbDrink.setSelectedItem("Select a drink");
				jcmbCurrency.setSelectedItem("Choose One");
				
			}
		});
		JbtnReset.setBounds(642, 24, 97, 25);
		panel_2_1.add(JbtnReset);
		
		JButton JbtnExit = new JButton("Exit");
		JbtnExit.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				System.exit(0);
			}
		});
		JbtnExit.setBounds(898, 24, 97, 25);
		panel_2_1.add(JbtnExit);
		
		JLabel lblNewLabel = new JLabel("Loan Management System");
		lblNewLabel.setFont(new Font("Tahoma", Font.BOLD, 40));
		lblNewLabel.setBounds(277, 32, 623, 59);
		frame.getContentPane().add(lblNewLabel);
	}
}
