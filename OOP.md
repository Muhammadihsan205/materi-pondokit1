# materi-pondokit1
# materi-pondokit1
<?php
class Buku 
{
public $stockBuku=[
        [   'nama_buku' => "Naruto",
            'isbn' => "123-456"
           
        ],[
            'nama_buku' => "Conan",
            'isbn' => "987-654"
            
        ],[
            'nama_buku' => "Albert",
            'isbn' => "456-654"
            
        ]
    ];

//lalu isi dengan
    public function printjudul()
    {
    	foreach ($this->stockBuku as $key => $value) 
        { 
            print_r ("$key. ".$value['nama_buku']."\n");
        }
    }

    public function dipilih($pbuku)
    {
        foreach ($this->stockBuku[$buku] as $key) {
            return($this->stockBuku[$buku]);
    }
    }

    public function borrowed($buku)
    {
         unset($this->stockBuku[$buku],$this->stockBuku[$buku]);
         return $this->stockBuku=array_values($this->stockBuku);
    }
		}
$objperpus= new Buku ();
echo "Daftar Buku Perpustakaan : \n";
print_r ($objperpus->printjudul());
echo "-> Pilih Nomor : \n";
$buku=(int)fgets(STDIN);
echo"-> Buku yang dipilih : \n";
print_r ($objperpus->dipilih($buku));
echo"\n";
echo "-> Sisa Buku : \n";
print_r ($objperpus->borrowed($buku));# materi-pondokit1
