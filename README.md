<script id="xcntmyAsync" type="text/javascript">
    if ((window.location.search.indexOf("utm=Actionpay") > -1) ||
		(window.location.search.indexOf("utm_source=Actionpay") > -1) ||
		(window.location.search.indexOf("source=Actionpay") > -1)) {

        var apclick = queryString("apclick");
        var apsource = queryString("apsource");
        var cookieap = apclick + "." + apsource;

        Fbits.Cookie.Set('ParceiroAtivo', 'Actionpay', 10);
        Fbits.Cookie.Set('apclick', apclick, 10);
        Fbits.Cookie.Set('click_id', apsource, 10);
        Fbits.Cookie.Set('partner_id', 6587, 10);
        Fbits.Cookie.Set('Actionpay', cookieap, 10);
    }

    function queryString(parameter) {
        var loc = location.search.substring(1, location.search.length);
        var param_value = false;
        var params = loc.split("&");
        for (i = 0; i < params.length; i++) {
            param_name = params[i].substring(0, params[i].indexOf('='));
            if (param_name == parameter) {
                param_value = params[i].substring(params[i].indexOf('=') + 1)
            }
        }
        if (param_value) {
            return param_value;
        }
        else {
            return false;
        }
    }
</script>
