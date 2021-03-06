# Virtual-machine
អត្ថបទស្ដីអំពីម៉ាសុីននិមិត្ត (Virtual Machine)

![VirtualBox](/src/img/vbox.png)

### ម៉ាស៊ីននិមិត្តVirtual Box (VB) ៖ 
*របៀបដំឡើង និងការបង្កើត virtual machine (បកបណ្ដោះអាសន្នថា ម៉ាស៊ីននិមិត្ត)​នៅលើលើUbuntu*

ការប្រើប្រាស់ប្រពន្ធ័ប្រតិបត្តការ (OS – Operating System) គឺសមស្របទៅតាមដំរូវការបស់យើងម្នាក់ៗ។ តែបើអ្នកចាំបាច់ប្រើប្រាស់OS​ (Windows, Linux, Mac OS,..) ផ្សេងគ្នានៅលើម៉ាស៊ីន (កុំព្យូទ័រ) តែមួយនោះអ្នកចាំបាច់ចេះពីរបៀបប្រើប្រាស់ម៉ាស៊ីននិមិត្ត។ ម៉ាស៊ីននិមិត្តដែលពេញនិយមសព្វថ្ងៃនេះគឺ Virtual Box និង Vmware។ នៅលើម៉ាស៊ីននិមិត្តនេះអ្នកអាចដំឡើងប្រពន្ធប្រតិបត្តការជាច្រើន និងយ៉ាងងាយស្រួល។
អត្ថបទនេះខ្ញុំនឹងរៀបរាប់មូលដ្ធានបំផុតពីVirtualbox ណែនាំក្បោះក្បាយពីរបៀបដំឡើងVirtualbox និងបង្កើតម៉ាស៊ីននិមិត្តលើLinux OS។<br/>

*និមិត្តកម្មនៅលើVirtualboxយ៉ាងដូចម្ដេច?* <br/>
  Virtualbox (Oracle VM VirtualBox) គឺជាផ្នែកទន់និមិត្តកម្មមិនគិតកំរៃ អាចដំណើរការOSជាច្រើននៅពេលតែមួយ។ Virtualbox ដំណើរការនៅលើប្រពន្ធប្រតិបត្តការដូចជា Linux (Ubuntu), OS X, Windows បានផ្ដល់អោយឥតគិតថ្លៃទាំងស្រុង និងងាយស្រួលប្រើប្រាស់។
វាបង្កើនលទ្ធភាពម៉ាស៊ីនបច្ចប្បន្នភាពរបស់អ្នក ដើម្បីអាចដំណើការ OS នៅខាងក្នុងម៉ាស៊ីននិមិត្ត)ច្រើននៅស្របពេល តែមួយ។
ប៉ុន្តែវាជាម៉ាស៊ីននិមិត្ត គឺមានចំនុចខ្សោយផងដែរដូចជា មិនអាចលេងGames ល្បើនយឺត និងផ្នែកទន់នៅលើម៉ាស៊ីននិមិត្ត និងម៉ាស៊ីនពិតមិនអាចមានទំនាក់ទំនងជាមួយគ្នា-ល-។ <br/>

#### អត្ថប្រយោជន៍៖ <br/>
Virtualbox ផ្ដល់អត្ថប្រយោជន៍ដូចជា៖<br/>
<ul>
<li>ដំណើរការOSច្រើននៅពេលតែមួយ</li>
<li>ងាយស្រួលនឹងដំឡើង</li>
<li>កាត់បន្ថយការចំណាយ</li>
</ul>

មុខងារសំខាន់ៗរបស់VirtualBox
ខាងក្រោមនេះខ្ញុំនិងរៀបរាប់យ៉ាងខ្លីពីមុខងារបស់VirtualBox៖
***
## 1. របៀបដំឡើង​ Oracle Virtual
ខាងក្រោមនេះជារបៀបដំឡើង VirtualBox នៅលើប្រពន្ធប្រតិបត្តការ Ubuntu៖<br/>
មានពីររបៀបក្នុងការដំឡើងគឺ ទីមួយដំឡើងដោយ PPA និងទីពីរដំឡើងដោយ​ file .deb។<br/>

### 1.1 របៀបដំឡើង `VirtualBox` ដោយ​ `PPA` នៅក្នុង`Ubuntu`
នេះគឺជារបៀបងាយបំផុតក្នុងការដំឡើង VirtualBox ជំនាន់ថ្មីបំផុត។​ របៀបនេះ ជួយអោយអ្នកដំឡើងបណ្ដារកញ្ចប់ (package) ដែលទាក់ទងនិង VirtualBox ដោយស្វ័យប្រវត្តន៍ ហើយអ្នកប្រើប្រាស់ VirtualBox ជំនាន់ថ្មីបំផុត ព្រោះវានឹងផ្ដល់នៅវា update ជាមួយប្រពន្ធ (system) នៅពេលមានជំនាន់ថ្មី -ល-<br/>
១. ប្រសិនបើកុំព្យូទ័ររបស់អ្នកធ្លាប់ដំឡើង (ជំនាន់ចាស់) អ្នកគួតែវាយបញ្ចូល ឃ្លាបញ្ជាខាងក្រោមដើម្បី លុបវាចោលមុនពេលដំឡើង
> sudo apt-get remove virtualbo-* 

២.​ ដំបូងអ្នកបន្ថែម PPA របស់VirtualBox ទៅក្នុងស្តុក Ubuntu
> echo "deb http://download.virtualbox.org/virtualbox/debian $(lsb_release -sc) contrib" | sudo tee -a /etc/apt/sources.list

៣. បន្ទាប់មកបន្ថែម public key អោយVirtualBox ដោយ apt-secure
> wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox_2016.asc -O- | sudo apt-key add -

៤. បន្ទាប់មកដំឡើង VirtualBox 5.1
> sudo apt-get update

> sudo apt-get install virtualbox-5.1

៥. ដំណើរការ VirtualBox
> virtualbox

### 1.2 របៀបដំឡើង VirtualBox ដោយ file deb ក្នុង Ubuntu
១. ប្រសិនបើកុំព្យូទ័ររបស់អ្នកធ្លាប់ដំឡើង (ជំនាន់ចាស់) អ្នកគួតែវាយបញ្ចូល ឃ្លាបញ្ជាខាងក្រោមដើម្បី លុបវាចោលមុនពេលដំឡើង
> sudo apt-get remove virtualbo-*

២. ទាញយក file deb ដើម្បីដំឡើង VirtualBox តាមរយៈដំណខាងក្រោ
> https://www.virtualbox.org/wiki/Linux_Downloads

៣. ដំឡើង VirtualBox អ្នកចុចពីរដងនៅលើ file ដែលមានកន្ទុយ .deb ឫក៏ វាយបញ្ចូលឃ្លាបញ្ជាខាងក្រោម ទៅលើ Terminal (ត្រូវចាំថា អ្នកត្រូវប្ដូរ Dircetory ដល់ Directory ដែលមាន file deb)
> sudo dpkg -i virtualbox-5.0

___

*References*
> https://tecadmin.net/install-oracle-virtualbox-on-ubuntu/

> http://ubuntuhandbook.org/index.php/2016/07/virtualbox-5-1-released/



