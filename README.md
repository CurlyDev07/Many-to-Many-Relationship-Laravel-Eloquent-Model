# Many-to-Many-Relationship-Eloquent-Laravel

Note: this tutorial is overriding the default behavior of laravel eloquent 

i have 3 tables, what i want to do is make a relationship between two tables

ex: i have 1st table users and  2nd table club
  then i will create a 3rd intermediary table and i will call it club_admins and let's assume that tbl has column of 
  * club_id which is the fk of the club tbl
  * admin_id which is the fk of the users tbl

then put this short code in the CLUB TABLE 

public function club_admins(){
      //@params    
      // 1st =  'Intermidiary tbl', 
      // 2nd 'fk column of the club class to club_admins tbl'
      // 3rd 'fk column of the users class to club_admins tbl'
      
      return $this->belongsToMany(User::class,  'club_admins', 'club_id', 'admin_id');
}
s
