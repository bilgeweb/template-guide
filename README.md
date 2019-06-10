# Template Guide
## Application
### header.php
#### 1- Meta Etiketleri
`<?=$meta->html; ?>`
#### 2- Html Dil Kodu
`<?=$lng; ?>`
#### 3- Header Dosyalarını Çağırmak (css, js)
`assets/<?=$template; ?>`
#### 4- Body Sub Kodu Eklemek
`<?=$meta->body_sub_code;?>`
#### 5- E-posta Eklemek
`<a href="mailto:<?=get_contact_info(1,'eposta',true);?>"><?=get_contact_info(1,'eposta',true);?></a>`
#### 6- Telefon Eklemek
`<a href="tel:<?=get_contact_info(1,'phone',true);?>"><?=get_contact_info(1,'phone',true);?></a>`
#### 7- Dil Switch Eklemek
`                    <?php
                        if(get_lang_control())
                        {
                            foreach (get_lang_list() as $key => $value) {
                                echo '
                                     <a href="'.$value->code.'"><img src="'.$value->image.'" alt="'.$value->name.'"></a>
                                ';
                            }
                        }
                    ?>`
#### 8- Üst Logo Eklemek (Renkli)
`<a href="<?=$lng;?>"><img src="<?=$themelogo;?>" alt="LOGO"></a>`
#### 9- Menü Bağlantılarını Eklemek

