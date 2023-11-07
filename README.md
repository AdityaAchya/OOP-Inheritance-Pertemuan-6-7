# OOP-Inheritance-Pertemuan-6-7

Nama : Aditya Achya Ananta Nur

NIM  : 312210714

Kelas : TI.22.B1

Matkul : Pemrograman Orientasi Objek

Dosen : Wiyanto, S.Kom., M.Kom

# Tugas Pertemuan 6 & 7

Membuat diagram class setter dan getter



    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    
    namespace Inheritance
    {
        public class Pegawai
        {
    
    
            private string nama;
            private double gajiPokok;
    
            public void setNama(string nama)
            {
                this.nama = nama;
            }
            public string getNama() { return this.nama; }
    
            public double getGajiPokok() { return this.gajiPokok; }
    
            public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }
    
            public void cetakinfo()
            {
    
                Console.WriteLine("Nama : " + this.nama);
                Console.WriteLine("Gapok : " + this.gajiPokok);
            }
        }
    
    
        public class manager : Pegawai
        {
    
            private double tunjangan;
    
            public void setTunjangan(double tunjangan) { this.tunjangan = tunjangan; }
            public double getTunjangan() { return this.tunjangan; }
    
            public new void cetakinfo()
            {
    
                base.cetakinfo();
                this.cetakTunjangan();
            }
            public void cetakTunjangan()
            {
                Console.WriteLine("Tunjangan Anda : " + this.tunjangan);
    
            }
        }
    
        public class Programmer : Pegawai
        {
            private double bonus;
    
    
            public void setBonus(double bonus) { this.bonus = bonus; }
    
            public double getBonus() { return this.bonus; }
    
            public new void cetakinfo()
            {
                base.cetakinfo();
                this.cetakBonus();
            }
            public void cetakBonus()
            {
                Console.WriteLine("Bonus : " + this.bonus);
    
    
            }
    
        }
        class program
        {
            static void Main(string[] args)
            {
                Console.WriteLine("==== PEGAWAI ====");
                Pegawai pegawai = new Pegawai();
                pegawai.setNama("M Muammar Bin Suwirto");
                pegawai.setGajiPokok(5100000);
                pegawai.cetakinfo();
                Console.WriteLine();
    
                Console.WriteLine("==== MANAGER ====");
                manager Manager = new manager();
                Manager.setNama("M Muammar Bin Suwirto");
                Manager.setGajiPokok(30000000);
                Manager.setTunjangan(50000000);
                Manager.cetakinfo();
                Console.WriteLine();
    
                Console.WriteLine("==== PROGRAMMER ====");
                Programmer programer = new Programmer();
                programer.setNama("M Muammar Bin Suwirto");
                programer.setGajiPokok(7000000);
                programer.setBonus(100000000);
                programer.cetakinfo();
                Console.WriteLine();
    
    
                Console.WriteLine("press anykey");
                Console.ReadKey();
            }
        }
    }

Hasilnya :


![Screenshot 2023-11-07 213912](https://github.com/AdityaAchya/OOP-Inheritance-Pertemuan-6-7/assets/123864099/1c9fedd5-84ac-4f0e-8207-d8ff39db1d4c)

