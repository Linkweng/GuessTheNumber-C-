using static System.Windows.Forms.VisualStyles.VisualStyleElement.Rebar;

namespace QuizGame
{
    public partial class Form1 : Form
    {
        Random random = new Random();

        int Guess = 0;
        int randomNumber = 0;

        String ConverterNum = " ";

        


        public Form1()
        {
            InitializeComponent();


            randomNumber = (random.Next(1, 100));

             ConverterNum = Convert.ToString(randomNumber);

                



        }

        private void buttonClicked(object sender, EventArgs e)
        {
           int  Guess = 0;

             int Answer = Convert.ToInt32(textBox1.Text);



            if (Answer == randomNumber)
            {
                textBox1.Select();

                textBox2.Text = "Your guess is right! ";
                    MessageBox.Show("Your guess is right!"); 
                
            }
            else if (Answer < randomNumber)
            {
                textBox2.Text = ConverterNum;
                textBox2.Text = "Your guess is Low! ";
                //MessageBox.Show("Your guess is low! ");
            }
            else if (Answer > randomNumber)
            {
                textBox2.Text = ConverterNum;
                textBox2.Text ="Your guess is High! ";
               // MessageBox.Show("Your guess is high! ");
            }
        }
    }
}
