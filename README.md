githup-repositories-API-Javascript - Hakkında
====================

Github API kullanılarak güncel repositories bilgileri alınması için hazırlandı. Bootstrap yardımıyla biraz geliştirdim. Responsive ve ajax kategorileme sistemi eklendi. Dileyen geliştiriciler alıp kendileri daha da geliştirmeye devam edebilirler.

Şuan stabil bir şekilde, tüm repo bilgilerini detaylı biçimde çekmektedir. Hangi bilgileri döndürdüğünü <a href="https://api.github.com/users/maxmanus16/repos" target="_blank">https://api.github.com/users/maxmanus16/repos</a> adresinden inceleyebilirsiniz.

Kullanımı da oldukça basit, aşağıdan inceleyebilirsiniz.

Ekran Görüntüsü - Demo
====================

<a href="http://fatihsoysal.com/lab/" target="_blank"><img src="http://i.hizliresim.com/77aQzY.png"></a>

Detaylı Bilgi
====================

Daha fazlası için: <a href="http://www.fatihsoysal.com/">http://www.fatihsoysal.com/<a/>

Kullanımı
====================

```javascript
<script type="text/javascript">
$( document ).ready(function() {
    $.ajax({
        type: "GET",
        url: "https://api.github.com/users/maxmanus16/repos",
        dataType: "json",
        success: function(result) {
            for( i in result ) {
                $("#repo_list").append(
                	console.log(result[i].name);
                	console.log(result[i].language);
                	console.log(result[i].description);
                );
                console.log("i: " + i);
            }
            console.log(result);
            $("#repo_count").append("Total repositories: " + result.length);
        }
    });
});
</script>
```
