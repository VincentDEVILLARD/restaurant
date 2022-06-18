<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>


<svelte:head>
    <title>Privatisation</title>
    <meta name="description" content="À propos de notre restaurant" />
    <style type="text/css">
        @import url(style.css);
    </style>
</svelte:head>

<style>
    .reservations-title-parallax{
      background-image: url(https://cdn.pixabay.com/photo/2016/11/18/15/53/breakfast-1835478_960_720.jpg);
      background-size: cover;
      background-position: center;
    }

    .ui-datepicker-div{
      position: absolute;
      top: 10419.2px;
      left: 482.4px;
      z-index: 1;
      display: block;
    }
  </style>

<body>
    <section id="table-reservations">

        <div class="reservations-title-parallax">
                        <div class="container">
                        <div class="section-title-container" style="height: 60px;">
                        <h2 class="section-title" style="color:#15027c;">Table Reservations</h2>
        
                        </div><!--.section-title-container-->
                        </div><!--.container-->
                        </div><!--.parallax-->
                        
                        <div class="container">
                        
         <div role="form" class="resa" id="resa-form">
         <form action="/#resa-form" method="post" class="resa-form" novalidate="novalidate">

        <p>Name <br>
            <span class="resa-form-control-wrap-your-name"><input type="text" name="your-name" value="" size="40" class="resa-form-control resa-text resa-validates-as-required" aria-required="true" aria-invalid="false" placeholder="Your name"></span> </p>
        <p>Phone number <br>
            <span class="resa-form-control-wrap-phone-number"><input type="tel" name="phone-number" value="" size="40" class="resa-form-control resa-text resa-tel resa-validates-as-required resa-validates-as-tel" aria-required="true" aria-invalid="false" placeholder="Your phone number"></span> </p>
        <p>Date <br>
            <span class="resa-form-control-wrap-date"><input type="text" name="date" value="" size="40" class="resa-form-control resa-date resa-validates-as-required hasDatepicker" aria-required="true" placeholder="Date of your reservation" id="date"> </span> </p>
        <p>Time <br>
            <span class="resa-form-control-wrap-time"><input type="text" name="time" value="" size="40" class="resa-form-control resa-date resa-time resa-validates-as-required hasDatepicker" aria-required="true" placeholder="Time of your reservation" id="time"> </span> </p>
        <p>Email <br>
            <span class="resa-form-control-wrap-your-email"><input type="email" name="your-email" value="" size="40" class="resa-form-control resa-text resa-email resa-validates-as-required resa-validates-as-email" aria-required="true" aria-invalid="false" placeholder="Your email"></span> </p>
        <p>Number of guests :<br>
            <span class="resa-form-control-wrap people"><input name="guests" value="" class="" type="number" placeholder="0"></span>
        </p>
        <input type="submit" value="Send" class="resa-form-control resa-submit btn-flat"><img class="ajax-loader" src="http://www.les-caracteres.com/wp-content/plugins/contact-form-7/images/ajax-loader.gif" alt="Sending..." style="visibility: hidden;"></p>
         </form></div>
                        
                        </div><!--.container-->
                        
        </section>
</body>


<script type="text/javascript">
    jQuery(function($){
        $('input[name="date"]').datepicker({"dateFormat":"dd/mm/yy","controlType":"slider","addSliderAccess":true,"sliderAccessArgs":{"touchonly":true},"stepHour":1,"stepMinute":1,"stepSecond":1}).datepicker('option', $.datepicker.regional['en']).datepicker('option', 'minDate', "").datepicker('option', 'maxDate', "").datepicker('refresh');
    });
</script>

<script type="text/javascript">
    jQuery(function($){
        $('input[name="time"]').timepicker({"timeFormat":"HH:mm","addSliderAccess":true,"sliderAccessArgs":{"touchonly":true}}).timepicker('option', $.datepicker.regional['fr']).timepicker('refresh');
    });
    </script>

<div id="ui-datepicker-div" class="ui-datepicker ui-widget ui-widget-content ui-helper-clearfix ui-corner-all">
    <div class="ui-datepicker-header ui-widget-header ui-helper-clearfix ui-corner-all" style="display: none;">
        <a class="ui-datepicker-prev ui-corner-all" data-handler="prev" data-event="click" title="Previous">
            <span class="ui-icon ui-icon-circle-triangle-w">Previous</span></a>
        <a class="ui-datepicker-next ui-corner-all" data-handler="next" data-event="click" title="Next">
            <span class="ui-icon ui-icon-circle-triangle-e">Next</span></a>
        <div class="ui-datepicker-title">
            <span class="ui-datepicker-month">June</span>&nbsp;<span class="ui-datepicker-year">2022</span></div>
    </div>
    <table class="ui-datepicker-calendar" style="display: none;">
        <thead><tr>
            <th scope="col"><span title="Monday">M</span></th>
            <th scope="col"><span title="Tuesday">T</span></th>
            <th scope="col"><span title="Wednesday">W</span></th>
            <th scope="col"><span title="Thursday">T</span></th>
            <th scope="col"><span title="Friday">F</span></th>
            <th scope="col" class="ui-datepicker-week-end"><span title="Saturday">S</span></th>
            <th scope="col" class="ui-datepicker-week-end"><span title="Sunday">S</span></th></tr>
        </thead>
        <tbody><tr>
            <td class=" ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td>
            <td class=" ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td>
            <!--Choix des jours-->
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">1</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">2</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">3</a></td>
            <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">4</a></td>
            <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">5</a></td></tr>
        <tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">6</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">7</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">8</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">9</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">10</a></td>
            <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">11</a></td>
            <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">12</a></td></tr>
        <tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">13</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">14</a></td>                <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">15</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">16</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">17</a></td>
            <td class=" ui-datepicker-week-end ui-datepicker-days-cell-over  ui-datepicker-today" data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default ui-state-highlight ui-state-hover" href="#">18</a></td>
            <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">19</a></td></tr>            <tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">20</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">21</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">22</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">23</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">24</a></td>                <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">25</a></td>
            <td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">26</a></td></tr>
        <tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">27</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">28</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">29</a></td>
            <td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">30</a></td>
            <td class=" ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td>                    <td class=" ui-datepicker-week-end ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td>                <td class=" ui-datepicker-week-end ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td></tr></tbody></table>
        
        <!--Choix de l'heure-->
        <div class="ui-timepicker-div">
            <div class="ui-widget-header ui-helper-clearfix ui-corner-all">
                <div class="ui-datepicker-title">Pick a time slot</div></div>
            <dl><dt class="ui_tpicker_time_label">Hour</dt>
                <dd class="ui_tpicker_time">00:00</dd>
                <dt class="ui_tpicker_hour_label">Hours</dt>
                <dd class="ui_tpicker_hour">
                    <div class="ui_tpicker_hour_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all">
                        <span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span>
                    </div></dd>
                <dt class="ui_tpicker_minute_label">Minutes</dt>
                <dd class="ui_tpicker_minute">
                    <div class="ui_tpicker_minute_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all">
                        <span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span>
                    </div></dd>
                <dt class="ui_tpicker_second_label" style="display:none;">Seconds</dt>
                <dd class="ui_tpicker_second">
                    <div class="ui_tpicker_second_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all" style="display:none;">
                        <span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span>
                    </div></dd>
            </dl>
        </div>
        <div class="ui-datepicker-buttonpane ui-widget-content">
            <button type="button" class="ui-datepicker-current ui-state-default ui-priority-secondary ui-corner-all" data-handler="today" data-event="click">Today</button>
            <button type="button" class="ui-datepicker-close ui-state-default ui-priority-primary ui-corner-all" data-handler="hide" data-event="click">Close</button>
        </div>
    </div>

::before

<div class="ui-datepicker-header ui-widget-header ui-helper-clearfix ui-corner-all" style="display: none;">
    <a class="ui-datepicker-prev ui-corner-all" data-handler="prev" data-event="click" title="Previous">
        <span class="ui-icon ui-icon-circle-triangle-w">Previous</span></a>
    <a class="ui-datepicker-next ui-corner-all" data-handler="next" data-event="click" title="Next">
        <span class="ui-icon ui-icon-circle-triangle-e">Next</span></a>
    <div class="ui-datepicker-title">
        <span class="ui-datepicker-month">june</span>&nbsp;<span class="ui-datepicker-year">2022</span></div></div>

<table class="ui-datepicker-calendar" style="display: none;"><thead><tr><th scope="col"><span title="lundi">L</span></th><th scope="col"><span title="mardi">M</span></th><th scope="col"><span title="mercredi">M</span></th><th scope="col"><span title="jeudi">J</span></th><th scope="col"><span title="vendredi">V</span></th><th scope="col" class="ui-datepicker-week-end"><span title="samedi">S</span></th><th scope="col" class="ui-datepicker-week-end"><span title="dimanche">D</span></th></tr></thead><tbody><tr><td class=" ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td><td class=" ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">1</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">2</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">3</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">4</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">5</a></td></tr><tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">6</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">7</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">8</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">9</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">10</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">11</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">12</a></td></tr><tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">13</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">14</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">15</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">16</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">17</a></td><td class=" ui-datepicker-week-end ui-datepicker-days-cell-over  ui-datepicker-today" data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default ui-state-highlight ui-state-hover" href="#">18</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">19</a></td></tr><tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">20</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">21</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">22</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">23</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">24</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">25</a></td><td class=" ui-datepicker-week-end " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">26</a></td></tr><tr><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">27</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">28</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">29</a></td><td class=" " data-handler="selectDay" data-event="click" data-month="5" data-year="2022"><a class="ui-state-default" href="#">30</a></td><td class=" ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td><td class=" ui-datepicker-week-end ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td><td class=" ui-datepicker-week-end ui-datepicker-other-month ui-datepicker-unselectable ui-state-disabled">&nbsp;</td></tr></tbody></table>

<div class="ui-timepicker-div"><div class="ui-widget-header ui-helper-clearfix ui-corner-all"><div class="ui-datepicker-title">Choisir une heure</div></div><dl><dt class="ui_tpicker_time_label">Heure</dt><dd class="ui_tpicker_time">00:00</dd><dt class="ui_tpicker_hour_label">Heures</dt><dd class="ui_tpicker_hour"><div class="ui_tpicker_hour_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all"><span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span></div></dd><dt class="ui_tpicker_minute_label">Minutes</dt><dd class="ui_tpicker_minute"><div class="ui_tpicker_minute_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all"><span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span></div></dd><dt class="ui_tpicker_second_label" style="display:none;">Secondes</dt><dd class="ui_tpicker_second"><div class="ui_tpicker_second_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all" style="display:none;"><span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span></div></dd><dt class="ui_tpicker_millisec_label" style="display:none;">Millisecondes</dt><dd class="ui_tpicker_millisec"><div class="ui_tpicker_millisec_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all" style="display:none;"><span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span></div></dd><dt class="ui_tpicker_microsec_label" style="display:none;">Microsecondes</dt><dd class="ui_tpicker_microsec"><div class="ui_tpicker_microsec_slider ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all" style="display:none;"><span class="ui-slider-handle ui-state-default ui-corner-all" tabindex="0" style="left: 0%;"></span></div></dd><dt class="ui_tpicker_timezone_label" style="display:none;">Fuseau horaire</dt><dd class="ui_tpicker_timezone" style="display:none;"><select><option value="-720">-1200</option><option value="-660">-1100</option><option value="-600">-1000</option><option value="-570">-0930</option><option value="-540">-0900</option><option value="-480">-0800</option><option value="-420">-0700</option><option value="-360">-0600</option><option value="-300">-0500</option><option value="-270">-0430</option><option value="-240">-0400</option><option value="-210">-0330</option><option value="-180">-0300</option><option value="-120">-0200</option><option value="-60">-0100</option><option value="0">+0000</option><option value="60">+0100</option><option value="120">+0200</option><option value="180">+0300</option><option value="210">+0330</option><option value="240">+0400</option><option value="270">+0430</option><option value="300">+0500</option><option value="330">+0530</option><option value="345">+0545</option><option value="360">+0600</option><option value="390">+0630</option><option value="420">+0700</option><option value="480">+0800</option><option value="525">+0845</option><option value="540">+0900</option><option value="570">+0930</option><option value="600">+1000</option><option value="630">+1030</option><option value="660">+1100</option><option value="690">+1130</option><option value="720">+1200</option><option value="765">+1245</option><option value="780">+1300</option><option value="840">+1400</option></select></dd></dl></div>
<div class="ui-datepicker-buttonpane ui-widget-content"><button type="button" class="ui-datepicker-current ui-state-default ui-priority-secondary ui-corner-all" data-handler="today" data-event="click">Aujourd'hui</button><button type="button" class="ui-datepicker-close ui-state-default ui-priority-primary ui-corner-all" data-handler="hide" data-event="click">Fermer</button></div>
::after