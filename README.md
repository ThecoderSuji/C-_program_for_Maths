using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
 
public class calculation
{
    public int a, b, ans;
    public void add()
    {
        ans = a + b;
    }
    public void sub()
    {
        ans = a - b;
    }
    public void mul()
    {
        ans = a * b;
    }
    public void div()
    {
        ans = a / b;
    }
}

namespace WebApplication3
{
    
    public partial class WebForm1 : System.Web.UI.Page
    {
        calculation c;
        protected void Page_Load(object sender, EventArgs e)
        {
            c= new calculation();
           
        }

        protected void Button1_Click(object sender, EventArgs e)
        {
            c.a = Convert.ToInt32(TextBox1.Text);
            c.b = Convert.ToInt32(TextBox2.Text);
            c.add();
            Label3.Text = c.ans.ToString();
        }

        protected void Button2_Click(object sender, EventArgs e)
        {
            c.a = Convert.ToInt32(TextBox1.Text);
            c.b = Convert.ToInt32(TextBox2.Text);
            c.sub();
            Label3.Text = c.ans.ToString();
        }

        protected void Button3_Click(object sender, EventArgs e)
        {
            c.a = Convert.ToInt32(TextBox1.Text);
            c.b = Convert.ToInt32(TextBox2.Text);
            c.mul();
            Label3.Text = c.ans.ToString();
        }

        protected void Button4_Click(object sender, EventArgs e)
        {
            c.a = Convert.ToInt32(TextBox1.Text);
            c.b = Convert.ToInt32(TextBox2.Text);
            c.div();
            Label3.Text = c.ans.ToString();
        }
    }
}
