using System;
					
public class Program
{
	public class People
	{ 
		private string name;
		private double teglo;
		private double rust;
		
		public People()
		{
			this.name="name";
				this.teglo=0;
			this.rust=0;
		}
		public People(string name, double teglo, double rust)
		{
			this.name=name;
				this.teglo=teglo;
			this.rust=rust;
		}
		public string Name
		{
			set{this.name=value;}
			get{return this.name;}
		}
		public double Teglo
			{
			set{this.teglo=value;}
			get{return this.teglo;}
		}
		public double Rust
			{
			set{this.rust=value;}
			get{return this.rust;}
		}
		public void Indecs()
		{
			double index=teglo/(rust*rust);
			Console.WriteLine("Indeks na telesnata vi masa e {0}", index);
						if(index<16){
			Console.WriteLine("Тежко недохранване");
			}else if(index<19){
					Console.WriteLine("Леко недохранване");
					}else if(index<25){
									Console.WriteLine("нормално тегло");	
									}else if(index<30)
											{
											Console.WriteLine("предзатлъстяване");
											}else{
												Console.WriteLine("затлъстяване");
						}
		}
	}
	public static void Main()
	{
		People s=new People();
		s.Name=Console.ReadLine();
		s.Teglo=double.Parse(Console.ReadLine());
		s.Rust=double.Parse(Console.ReadLine());
		s.Indecs();
		
		
	}
}
