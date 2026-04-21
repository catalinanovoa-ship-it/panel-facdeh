<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Panel de Gestión · FACDEH · UCen</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--bg:#fff;--bg2:#f5f5f3;--bg3:#eeeee9;--txt:#1a1a18;--t2:#6b6b66;--t3:#9b9b95;--bd:rgba(0,0,0,.10);--bd2:rgba(0,0,0,.20);--acc:#0057a8;--F:-apple-system,BlinkMacSystemFont,'Segoe UI',Arial,sans-serif}
@media(prefers-color-scheme:dark){:root{--bg:#1e1e1c;--bg2:#2a2a28;--bg3:#333330;--txt:#f0f0ec;--t2:#a8a8a2;--t3:#707070;--bd:rgba(255,255,255,.10);--bd2:rgba(255,255,255,.20)}}
body{font-family:var(--F);background:var(--bg3);min-height:100vh;display:flex;align-items:flex-start;justify-content:center;padding:1.5rem 1rem}
.panel{display:flex;border:.5px solid var(--bd);border-radius:12px;overflow:hidden;width:100%;max-width:980px;min-height:580px;background:var(--bg)}
/* SIDEBAR */
.sb{width:205px;background:var(--bg2);border-right:.5px solid var(--bd);display:flex;flex-direction:column;flex-shrink:0;padding:1rem 0}
.sb-top{padding:0 1rem 1rem;border-bottom:.5px solid var(--bd);margin-bottom:.5rem}
.logobox{width:30px;height:30px;border-radius:6px;background:var(--acc);display:flex;align-items:center;justify-content:center}
.nb{display:flex;align-items:center;gap:8px;padding:7px 10px;border-radius:6px;cursor:pointer;font-size:13px;border:none;background:none;width:100%;text-align:left;margin-bottom:2px;font-family:var(--F);color:var(--t2);transition:all .12s}
.nb:hover{background:var(--bg);color:var(--txt)}
.nb.on{background:var(--bg);color:var(--txt);font-weight:500;border:.5px solid var(--bd)}
.slbl{font-size:10px;font-weight:500;color:var(--t3);text-transform:uppercase;letter-spacing:.07em;padding:.5rem .4rem .3rem;display:block}
/* MAIN */
.main{flex:1;overflow-y:auto;background:var(--bg)}
.pg{display:none;padding:1.5rem}
.pg.on{display:block}
.ph{display:flex;align-items:center;justify-content:space-between;margin-bottom:1.25rem;padding-bottom:1rem;border-bottom:.5px solid var(--bd)}
.pt{font-size:18px;font-weight:500;color:var(--txt);margin-bottom:3px}
.ps{font-size:13px;color:var(--t2)}
/* METRICAS */
.mg{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:10px;margin-bottom:1.5rem}
.mc{background:var(--bg2);border-radius:8px;padding:1rem}
/* BANNER PEC */
.banner{background:var(--acc);border-radius:10px;padding:1rem 1.25rem;margin-bottom:1.25rem;cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:1rem}
.banner:hover{opacity:.92}
/* INICIO GRID */
.twocol{display:grid;grid-template-columns:1fr 1fr;gap:1.25rem}
.rrow{display:flex;align-items:center;gap:10px;padding:.75rem;background:var(--bg2);border-radius:8px;cursor:pointer;margin-bottom:6px;border-left:3px solid var(--acc)}
.rrow:hover{background:var(--bg3)}
.ib{width:32px;height:32px;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:9.5px;font-weight:500;flex-shrink:0}
/* BUSCADOR + PILLS */
.sbox{display:flex;align-items:center;gap:8px;background:var(--bg2);border:.5px solid var(--bd);border-radius:8px;padding:7px 12px;margin-bottom:.75rem}
.sbox input{border:none;background:none;outline:none;flex:1;font-size:13px;color:var(--txt);font-family:var(--F)}
.pills{display:flex;gap:6px;margin-bottom:1rem;flex-wrap:wrap}
.pill{font-size:11.5px;padding:4px 10px;border-radius:20px;cursor:pointer;background:none;color:var(--t2);border:.5px solid var(--bd2);font-family:var(--F);transition:all .1s}
.pill.on{background:var(--acc);color:#fff;border-color:var(--acc)}
/* DOC ROW */
.dr{display:flex;align-items:center;gap:10px;padding:.7rem 1rem;background:var(--bg);border:.5px solid var(--bd);border-radius:10px;cursor:pointer;transition:background .12s;margin-bottom:6px}
.dr:hover{background:var(--bg2)}
.bv{font-size:11px;padding:2px 8px;background:#EAF3DE;color:#27500A;border-radius:20px;white-space:nowrap;flex-shrink:0}
/* POLICY CARDS */
.pgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:10px}
.pcard{background:var(--bg);border:.5px solid var(--bd);border-radius:12px;padding:1.1rem;cursor:pointer;transition:border-color .15s}
.pcard:hover{border-color:var(--bd2)}
/* NORMATIVA */
.na{margin-bottom:1.25rem}
.na-hd{display:flex;align-items:center;gap:8px;margin-bottom:.6rem}
.nt{border:.5px solid var(--bd);border-radius:8px;overflow:hidden}
.nth{display:grid;grid-template-columns:1fr 130px 60px;background:var(--bg2);padding:6px 12px;font-size:11px;font-weight:500;color:var(--t3);border-bottom:.5px solid var(--bd)}
.nr{display:grid;grid-template-columns:1fr 130px 60px;padding:8px 12px;font-size:12.5px;cursor:pointer;border-top:.5px solid var(--bd);transition:background .1s}
.nr:first-of-type{border-top:none}
.nr:hover{background:var(--bg2)}
/* CALENDARIOS */
.cgrid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
/* MODAL */
.mbg{display:none;position:fixed;inset:0;background:rgba(0,0,0,.45);z-index:999;align-items:center;justify-content:center;padding:1rem}
.mbg.on{display:flex}
.mbox{background:var(--bg);border-radius:14px;width:100%;max-width:560px;max-height:88vh;overflow-y:auto}
.mhd{padding:1.25rem 1.25rem .875rem;border-bottom:.5px solid var(--bd);display:flex;align-items:flex-start;gap:12px;position:sticky;top:0;background:var(--bg);border-radius:14px 14px 0 0;z-index:2}
.mico{width:38px;height:38px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:10px;font-weight:600;flex-shrink:0}
.mcls{background:var(--bg2);border:none;border-radius:50%;width:28px;height:28px;cursor:pointer;font-size:18px;color:var(--t2);display:flex;align-items:center;justify-content:center;flex-shrink:0}
.mbdy{padding:1.25rem}
.ficha{background:var(--bg2);border-radius:8px;padding:.875rem 1rem;margin-bottom:1.25rem;display:flex;flex-direction:column;gap:6px}
.fr{display:flex;gap:8px;font-size:12.5px}
.fl{color:var(--t2);min-width:72px;flex-shrink:0;line-height:1.4}
.fv{color:var(--txt);line-height:1.4}
.slbl2{font-size:10.5px;font-weight:600;color:var(--t3);text-transform:uppercase;letter-spacing:.07em;margin-bottom:6px}
.mpts{font-size:12.5px;color:var(--txt);padding-left:1.25rem;line-height:1.6}
.mpts li{margin-bottom:6px}
</style>
</head>
<body>
<div class="panel">

<!-- SIDEBAR -->
<div class="sb">
  <div class="sb-top">
    <div style="display:flex;align-items:center;gap:9px">
      <div class="logobox"><svg width="16" height="16" viewBox="0 0 16 16" fill="none"><rect x="2" y="2" width="12" height="8" rx="1.5" fill="white" opacity=".9"/><rect x="5.5" y="11" width="5" height="2" rx="1" fill="white" opacity=".6"/></svg></div>
      <div><div style="font-size:12.5px;font-weight:500;color:var(--txt)">FACDEH</div><div style="font-size:10.5px;color:var(--t3)">UCen · 2026</div></div>
    </div>
  </div>
  <div style="padding:0 .6rem;flex:1">
    <span class="slbl">Principal</span>
    <button class="nb on" id="nb-inicio" onclick="nav('inicio')">
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" style="flex-shrink:0"><rect x="1" y="1" width="5.5" height="5.5" rx="1.5" fill="currentColor" opacity=".9"/><rect x="7.5" y="1" width="5.5" height="5.5" rx="1.5" fill="currentColor" opacity=".4"/><rect x="1" y="7.5" width="5.5" height="5.5" rx="1.5" fill="currentColor" opacity=".4"/><rect x="7.5" y="7.5" width="5.5" height="5.5" rx="1.5" fill="currentColor" opacity=".7"/></svg>
      <span>Inicio</span></button>
    <button class="nb" id="nb-resoluciones" onclick="nav('resoluciones')">
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" style="flex-shrink:0"><rect x="2.5" y="1" width="9" height="12" rx="1.5" fill="none" stroke="currentColor" stroke-width="1.2"/><line x1="5" y1="4.5" x2="9" y2="4.5" stroke="currentColor" stroke-width="1"/><line x1="5" y1="7" x2="9" y2="7" stroke="currentColor" stroke-width="1"/><line x1="5" y1="9.5" x2="7.5" y2="9.5" stroke="currentColor" stroke-width="1"/></svg>
      <span>Resoluciones</span></button>
    <button class="nb" id="nb-politicas" onclick="nav('politicas')">
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" style="flex-shrink:0"><path d="M7 1L8.6 4.8H12.5L9.5 7.2L10.5 11L7 8.8L3.5 11L4.5 7.2L1.5 4.8H5.4Z" fill="none" stroke="currentColor" stroke-width="1.1" stroke-linejoin="round"/></svg>
      <span>Políticas</span></button>
    <button class="nb" id="nb-normativa" onclick="nav('normativa')">
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" style="flex-shrink:0"><circle cx="7" cy="7" r="5.5" fill="none" stroke="currentColor" stroke-width="1.2"/><line x1="7" y1="4" x2="7" y2="7.5" stroke="currentColor" stroke-width="1.2" stroke-linecap="round"/><circle cx="7" cy="9.5" r=".8" fill="currentColor"/></svg>
      <span>Normativa</span></button>
    <button class="nb" id="nb-calendarios" onclick="nav('calendarios')">
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" style="flex-shrink:0"><rect x="1.5" y="2.5" width="11" height="10" rx="1.5" fill="none" stroke="currentColor" stroke-width="1.2"/><line x1="1.5" y1="5.5" x2="12.5" y2="5.5" stroke="currentColor" stroke-width="1"/><line x1="4.5" y1="1" x2="4.5" y2="4" stroke="currentColor" stroke-width="1.2" stroke-linecap="round"/><line x1="9.5" y1="1" x2="9.5" y2="4" stroke="currentColor" stroke-width="1.2" stroke-linecap="round"/></svg>
      <span>Calendarios 2026</span></button>
  </div>
  <div style="padding:.75rem 1rem 0;border-top:.5px solid var(--bd)">
    <div style="font-size:11px;color:var(--t3)">Universidad Central de Chile</div>
    <div style="font-size:10.5px;color:var(--t3)">FACDEH · Panel de Gestión</div>
  </div>
</div>

<!-- MAIN -->
<div class="main" id="main">

<!-- INICIO -->
<div id="pg-inicio" class="pg on">
  <div class="ph">
    <div><div class="pt">Panel de Gestión · FACDEH</div><div class="ps">Facultad de Derecho y Humanidades · Universidad Central de Chile</div></div>
    <div style="font-size:11.5px;color:var(--t3);background:var(--bg2);padding:4px 10px;border-radius:20px;border:.5px solid var(--bd)">2026</div>
  </div>
  <div class="mg">
    <div class="mc"><div style="font-size:11.5px;color:var(--t2);margin-bottom:4px">Documentos</div><div style="font-size:24px;font-weight:500;color:var(--txt)">30</div><div style="font-size:11px;color:var(--t3)">activos 2026</div></div>
    <div class="mc"><div style="font-size:11.5px;color:var(--t2);margin-bottom:4px">Calendarios</div><div style="font-size:24px;font-weight:500;color:var(--txt)">5</div><div style="font-size:11px;color:var(--t3)">régimen 2026</div></div>
    <div class="mc"><div style="font-size:11.5px;color:var(--t2);margin-bottom:4px">Instructivos</div><div style="font-size:24px;font-weight:500;color:var(--txt)">3</div><div style="font-size:11px;color:var(--t3)">normas carrera</div></div>
    <div class="mc"><div style="font-size:11.5px;color:var(--t2);margin-bottom:4px">Áreas</div><div style="font-size:24px;font-weight:500;color:var(--txt)">9</div><div style="font-size:11px;color:var(--t3)">de gestión</div></div>
  </div>
  <div class="banner" onclick="openDoc('pec3142')">
    <div><div style="font-size:10px;font-weight:500;color:rgba(255,255,255,.65);text-transform:uppercase;letter-spacing:.07em;margin-bottom:3px">Nuevo · Res. 3142 · 01 abril 2026</div><div style="font-size:14px;font-weight:500;color:#fff">Plan Estratégico Corporativo 2026–2032</div><div style="font-size:12px;color:rgba(255,255,255,.7);margin-top:2px">Aprobado por Junta Directiva en sesión N°852 · Ver ficha →</div></div>
    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" style="flex-shrink:0;opacity:.7"><path d="M5 10h10M11 6l4 4-4 4" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
  </div>
  <div class="twocol">
    <div>
      <div style="font-size:13px;font-weight:500;color:var(--txt);margin-bottom:.75rem">Novedades 2026</div>
      <div class="rrow" onclick="openDoc('nor07')"><div class="ib" style="background:#EEEDFE;color:#3C3489">NOR</div><div><div style="font-size:12.5px;font-weight:500;color:var(--txt)">Normas Académicas Derecho Diurno</div><div style="font-size:11px;color:var(--t3)">Res. 07/2026 · Plan DE04</div></div></div>
      <div class="rrow" onclick="openDoc('nor08')" style="border-color:#534AB7"><div class="ib" style="background:#EEEDFE;color:#3C3489">NOR</div><div><div style="font-size:12.5px;font-weight:500;color:var(--txt)">Normas Académicas Derecho Vespertino</div><div style="font-size:11px;color:var(--t3)">Res. 08/2026 · Plan DV03</div></div></div>
      <div class="rrow" onclick="openDoc('nor06')" style="border-color:#0F6E56"><div class="ib" style="background:#E1F5EE;color:#085041">NOR</div><div><div style="font-size:12.5px;font-weight:500;color:var(--txt)">Normas Académicas Trabajo Social</div><div style="font-size:11px;color:var(--t3)">Res. 06/2026 · Plan 2025</div></div></div>
      <div class="rrow" onclick="openDoc('res7470')" style="border-color:#D4537E"><div class="ib" style="background:#FBEAF0;color:#72243E">GEN</div><div><div style="font-size:12.5px;font-weight:500;color:var(--txt)">Reglamento Acoso Sexual y Violencia de Género</div><div style="font-size:11px;color:var(--t3)">Res. 7470 · Octubre 2025</div></div></div>
    </div>
    <div>
      <div style="font-size:13px;font-weight:500;color:var(--txt);margin-bottom:.75rem">Áreas de gestión</div>
      <div id="areas-list"></div>
    </div>
  </div>
</div>

<!-- RESOLUCIONES -->
<div id="pg-resoluciones" class="pg">
  <div class="ph"><div><div class="pt">Resoluciones</div><div class="ps">30 documentos · Haz clic para ver ficha completa</div></div></div>
  <div class="sbox"><svg width="13" height="13" viewBox="0 0 13 13" fill="none" style="flex-shrink:0;opacity:.4"><circle cx="5" cy="5" r="3.8" fill="none" stroke="currentColor" stroke-width="1.3"/><line x1="7.8" y1="7.8" x2="11.5" y2="11.5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/></svg><input id="srch" oninput="renderDocs()" placeholder="Buscar por nombre, número o materia..."></div>
  <div class="pills">
    <button class="pill on" onclick="setF('todos',this)">Todos</button>
    <button class="pill" onclick="setF('calendario',this)">Calendarios</button>
    <button class="pill" onclick="setF('estrategico',this)">Estratégico</button>
    <button class="pill" onclick="setF('academico',this)">Académico</button>
    <button class="pill" onclick="setF('inclusion',this)">Inclusión</button>
    <button class="pill" onclick="setF('compliance',this)">Compliance</button>
    <button class="pill" onclick="setF('docencia',this)">Docencia</button>
    <button class="pill" onclick="setF('vcm',this)">VcM</button>
  </div>
  <div id="dl"></div>
</div>

<!-- POLÍTICAS -->
<div id="pg-politicas" class="pg">
  <div class="ph"><div><div class="pt">Políticas Institucionales</div><div class="ps">Haz clic para ver la ficha completa</div></div></div>
  <div class="pgrid" id="pgrid"></div>
</div>

<!-- NORMATIVA -->
<div id="pg-normativa" class="pg">
  <div class="ph"><div><div class="pt">Normativa por Área</div><div class="ps">Haz clic en cualquier fila para ver la ficha completa</div></div></div>
  <div id="norm"></div>
</div>

<!-- CALENDARIOS -->
<div id="pg-calendarios" class="pg">
  <div class="ph"><div><div class="pt">Calendarios Académicos 2026</div><div class="ps">Haz clic para ver todas las fechas</div></div></div>
  <div class="cgrid" id="cgrid"></div>
</div>

</div><!-- /main -->
</div><!-- /panel -->

<!-- MODAL -->
<div class="mbg" id="mbg" onclick="if(event.target===this)closeModal()">
  <div class="mbox">
    <div class="mhd">
      <div class="mico" id="m-ico"></div>
      <div style="flex:1;min-width:0">
        <div style="display:flex;align-items:center;gap:8px;margin-bottom:4px;flex-wrap:wrap">
          <span id="m-badge" style="font-size:10.5px;font-weight:600;padding:2px 9px;border-radius:20px"></span>
          <span id="m-res" style="font-size:11px;color:var(--t3)"></span>
        </div>
        <div id="m-title" style="font-size:15px;font-weight:500;color:var(--txt);line-height:1.3"></div>
      </div>
      <button class="mcls" onclick="closeModal()">&#215;</button>
    </div>
    <div class="mbdy">
      <div class="ficha">
        <div class="fr"><span class="fl">Materia</span><span class="fv" id="m-mat"></span></div>
        <div class="fr"><span class="fl">Fecha</span><span class="fv" id="m-fecha"></span></div>
        <div class="fr"><span class="fl">Firmantes</span><span class="fv" id="m-firm"></span></div>
      </div>
      <div style="margin-bottom:1.25rem"><div class="slbl2">Resumen</div><p id="m-txt" style="font-size:13px;color:var(--txt);line-height:1.6"></p></div>
      <div><div class="slbl2">Puntos clave</div><ul class="mpts" id="m-pts"></ul></div>
      <div style="border-top:.5px solid var(--bd);padding-top:1rem;display:flex;gap:8px;justify-content:flex-end;margin-top:1rem">
        <button onclick="closeModal()" style="padding:7px 16px;background:none;border:.5px solid var(--bd2);border-radius:8px;font-size:13px;cursor:pointer;color:var(--t2);font-family:var(--F)">Cerrar</button>
        <button onclick="closeModal()" style="padding:7px 18px;background:var(--acc);border:none;border-radius:8px;font-size:13px;cursor:pointer;color:#fff;font-family:var(--F);font-weight:500">Aceptar</button>
      </div>
    </div>
  </div>
</div>

<script>
// -- BASE DE DATOS COMPLETA (30 documentos) ----------------------------------
var DB = {
pec3142:{ico:'PEC',bg:'#E6F1FB',fg:'#0C447C',cat:'estrategico',catL:'Plan estratégico',
  title:'Plan Estratégico Corporativo 2026-2032',res:'3142',year:'2026',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba el nuevo Plan Estratégico Corporativo 2026-2032 de la Universidad Central de Chile.',
  fecha:'Santiago, 01 de abril de 2026',
  firm:'Neftalí Carabantes Hernández (Secretario General) · Santiago González Larraín (Rector)',
  txt:'Instrumento rector del desarrollo institucional de la UCEN para 2026-2032, aprobado unánimemente por la Junta Directiva en sesión N°852 del 16 de diciembre de 2025. Proyecta la universidad hacia su cincuentenario como institución inclusiva, sostenible y de excelencia académica.',
  pts:['Promulga el Acuerdo N°2 de la Sesión Ordinaria N°852 de la Junta Directiva (16 diciembre 2025).','Promueve el fortalecimiento mediante autonomía, excelencia, responsabilidad social, generación de conocimiento e innovación.','Formulado a través de un proceso participativo y colaborativo que refleja la madurez institucional.','El texto íntegro del Plan se anexa a la resolución.','Deroga el PEC 2021-2025 (Res. 1006/2021) y su actualización (Res. 8199/2023).']},

pgd3165:{ico:'PGD',bg:'#E6F1FB',fg:'#0C447C',cat:'estrategico',catL:'Plan estratégico',
  title:'Políticas Globales de Desarrollo',res:'3165',year:'',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba las Políticas Globales de Desarrollo de la Universidad Central de Chile.',
  fecha:'Universidad Central de Chile',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Marco estratégico que define los lineamientos institucionales de desarrollo para la UCEN, articulando misión, visión y valores como base de los planes estratégicos corporativos.',
  pts:['Valores: Excelencia, Integridad, Libertad, Tolerancia, Solidaridad, Justicia, Dignidad.','Misión: entregar educación superior de excelencia y formación integral.','Visión: ser una universidad vinculada con la sociedad con posición consolidada en Santiago y La Serena.','Orienta el desarrollo en docencia, investigación, VcM y gestión institucional.','Sirve de marco de referencia para los Planes Estratégicos de cada período.']},

calpgsem:{ico:'CAL',bg:'#E6F1FB',fg:'#0C447C',cat:'calendario',catL:'Calendario 2026',
  title:'Calendario Postgrado Semestral 2026 -- Santiago',res:'0036',year:'2026',
  mat:'Fija Calendario de Actividades de Postgrado del año académico 2026, para programas en régimen semestral de Santiago.',
  fecha:'Santiago, 05 de enero de 2026',
  firm:'Emilio Oñate Vera (Vicerrector Académico) · Santiago González Larraín (Rector) · Neftalí Carabantes Hernández (Secretario General)',
  txt:'Calendario académico oficial para todos los programas de postgrado semestral de Santiago. Ningún programa puede exceder el 31 de diciembre de 2026.',
  pts:['Vacaciones de verano: 02 febrero - 01 marzo 2026.','Inscripción asignaturas 1°sem: 16-27 marzo 2026.','INICIO CLASES 1° semestre: 06 de abril de 2026.','Recesos: 02 mayo · 22-23 mayo 2026.','Encuesta docente: 22 junio - 08 julio 2026.','TÉRMINO 1° semestre (cierre actas): 08 de julio de 2026.','Inscripción asignaturas 2°sem: 10-18 agosto 2026.','INICIO CLASES 2° semestre: 24 de agosto de 2026.','Receso Fiestas Patrias: 14-17 septiembre 2026.','TÉRMINO 2° semestre (cierre actas): 31 de diciembre de 2026.','Recesos fin de año: 07 dic · 26 dic 2026 · 02 ene 2027.']},

calpgtri:{ico:'CAL',bg:'#E6F1FB',fg:'#0C447C',cat:'calendario',catL:'Calendario 2026',
  title:'Calendario Postgrado Trimestral 2026 -- Santiago',res:'0039',year:'2026',
  mat:'Fija Calendario de Actividades de Postgrado del año académico 2026, para programas en régimen trimestral de Santiago.',
  fecha:'Santiago, 05 de enero de 2026',
  firm:'Emilio Oñate Vera (Vicerrector Académico) · Santiago González Larraín (Rector) · Neftalí Carabantes Hernández (Secretario General)',
  txt:'Calendario para postgrado trimestral de Santiago. Ningún programa puede exceder el 30 de enero de 2027.',
  pts:['Vacaciones de verano: 02 febrero - 01 marzo 2026.','INICIO CLASES 1° trimestre: 06 de abril de 2026.','Recesos: 02 mayo · 22-23 mayo 2026.','TÉRMINO 1° trimestre (cierre actas): 04 de julio de 2026.','INICIO CLASES 2° trimestre: 20 de julio de 2026.','Receso Fiestas Patrias: 14-19 septiembre 2026.','TÉRMINO 2° trimestre (cierre actas): 24 de octubre de 2026.','INICIO CLASES 3° trimestre: 02 de noviembre de 2026.','TÉRMINO 3° trimestre (cierre actas): 30 de enero de 2027.','Recesos: 07 dic 2026 · 26 dic 2026 · 02 ene 2027.']},

calpregsem:{ico:'CAL',bg:'#E1F5EE',fg:'#085041',cat:'calendario',catL:'Calendario 2026',
  title:'Calendario Pregrado Semestral 2026 -- Stgo & Coquimbo',res:'0040',year:'2026',
  mat:'Fija Calendario de Actividades del año académico 2026 para carreras en régimen semestral de Santiago y Sede Región de Coquimbo.',
  fecha:'Santiago, 05 de enero de 2026',
  firm:'Emilio Oñate Vera (Vicerrector Académico) · Santiago González Larraín (Rector) · Neftalí Carabantes Hernández (Secretario General)',
  txt:'Calendario oficial para todas las carreras de pregrado semestral de Santiago y Coquimbo, jornadas diurna y vespertina.',
  pts:['Vacaciones de verano: 02 - 28 febrero 2026.','INICIO CLASES 1°sem (estudiantes nuevos): 09 de marzo 2026.','Nivelación estudiantes nuevos: 09-20 marzo 2026.','INICIO CLASES 1°sem (estudiantes antiguos): 23 de marzo de 2026.','Recesos: 02 mayo · 18-20 mayo (pausa académica) · 22-23 mayo 2026.','Exámenes 1°semestre: 20-30 julio 2026.','TÉRMINO 1°semestre (cierre actas): 31 de julio de 2026.','Vacaciones invierno: 03-14 agosto 2026.','INICIO CLASES 2° semestre: 17 de agosto de 2026.','Receso Fiestas Patrias: 14-17 septiembre 2026.','Exámenes 2°semestre: 14-23 diciembre 2026.','TÉRMINO 2°semestre (cierre actas): 24 de diciembre de 2026.']},

calpregtri:{ico:'CAL',bg:'#E1F5EE',fg:'#085041',cat:'calendario',catL:'Calendario 2026',
  title:'Calendario Pregrado Trimestral 2026 -- Advance & Vespertino',res:'0041',year:'2026',
  mat:'Fija Calendario del año académico 2026 para Carreras Vespertinas y Programas Advance en régimen trimestral de Santiago y Coquimbo.',
  fecha:'Santiago, 05 de enero de 2026',
  firm:'Emilio Oñate Vera (Vicerrector Académico) · Santiago González Larraín (Rector) · Neftalí Carabantes Hernández (Secretario General)',
  txt:'Calendario para carreras vespertinas y programas Advance en régimen trimestral de Santiago y Coquimbo.',
  pts:['Vacaciones de verano: 02 febrero - 01 marzo 2026.','Inscripción 1°trimestre: 02-13 marzo. Aula Digital: 16-20 marzo 2026.','INICIO CLASES 1° trimestre: 23 de marzo de 2026.','Recesos: 02 mayo · 22-23 mayo 2026.','TÉRMINO 1° trimestre (cierre actas): 21 de junio de 2026.','INICIO CLASES 2° trimestre: 06 de julio de 2026.','Receso Fiestas Patrias: 14-17 septiembre 2026.','TÉRMINO 2° trimestre (cierre actas): 11 de octubre de 2026.','INICIO CLASES 3° trimestre: 26 de octubre de 2026.','TÉRMINO 3° trimestre (cierre actas): 24 de enero de 2027.','Recesos fin de año: 07 dic 2026 · 26 dic 2026 · 02 ene 2027.']},

calvriip:{ico:'CNI',bg:'#FAEEDA',fg:'#633806',cat:'calendario',catL:'Investigación VRIIP',
  title:'Concursos Internos 2026 -- VRIIP',res:'VRIIP',year:'2026',
  mat:'Calendario de Concursos Internos 2026 de la Vicerrectoría de Investigación, Innovación y Postgrado. Dirigido a académicos e investigadores.',
  fecha:'Enero 2026',firm:'Vicerrectoría de Investigación, Innovación y Postgrado (VRIIP) · Universidad Central de Chile',
  txt:'Programa con 20 concursos internos VRIIP distribuidos en dos semestres. Cubre investigación científica, innovación, publicaciones, formación y congresos. Calendario sujeto a modificaciones.',
  pts:['Puente de Investigación: apertura 12 enero, cierre 29 abril.','Fomento a la Productividad: apertura 12 enero, cierre 12 marzo.','Publicaciones indexadas 1ª conv.: apertura 15 enero, cierre 15 marzo.','Semillas / Cataliza / FIT 2026: apertura 15 enero, cierre 22 abril.','Impulso a la Investigación Científica: apertura 30 enero, cierre 10 abril.','Investigación Sin Fronteras: apertura 30 enero, cierre 25 marzo.','Beca Semillero I+D+i: apertura 5 marzo, cierre 15 marzo.','Publicaciones 2ª conv.: apertura 16 abril, cierre 14 mayo.','XVI Concurso apoyo a congresos: apertura 17 mayo, cierre 15 junio.','Publicaciones 4ª conv. (2°sem): apertura 7 julio, cierre 3 agosto.','Taller de Escritura Santiago y Coquimbo: apertura 13 julio, cierre 7 agosto.','Publicaciones 5ª conv. (arrastre 2027): apertura 4 sep, cierre 30 oct.','Libros y capítulos (arrastre 2027): apertura 4 sep, cierre 30 oct.']},

rge9842:{ico:'RGE',bg:'#EEEDFE',fg:'#3C3489',cat:'academico',catL:'Reglamento',
  title:'Reglamento General de Estudios de Pregrado',res:'9842',year:'2023',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba nuevo Reglamento General de Estudios de Pregrado de la Universidad Central de Chile.',
  fecha:'Santiago, 29 de diciembre de 2023',
  firm:'Neftalí Carabantes Hernández (Secretario General) · Santiago González Larraín (Rector)',
  txt:'Marco normativo general vigente desde el 04 de marzo de 2024. Regula admisión, permanencia, evaluación y titulación para todas las carreras de pregrado de la UCEN.',
  pts:['Semestre: 18 semanas lectivas. Trimestre: 13 semanas lectivas. SCT como unidad de crédito.','Admisión: vías de ingreso, renovación de matrícula, desertor = sin matrícula 2 años consecutivos.','Evaluación: escala 1,0-7,0, nota mínima de aprobación 4,0, exigencia 60%.','Asistencia mínima: 75% en todas las asignaturas.','Art. 27: notas deben publicarse en 4 días hábiles (trimestre) o 10 días hábiles (semestre).','Art. 51: causales de eliminación: reprobar en 2ª oportunidad; reprobar en 3ª oportunidad; reprobar más del 50% de asignaturas inscritas.','Art. 52: apelación: Dirección de Carrera → Decanato → Dirección de Gestión de la Docencia.','Vigencia: desde 04 de marzo de 2024. Deroga Res. N°0112/1991 y todas sus modificaciones.']},

nor07:{ico:'NOR',bg:'#EEEDFE',fg:'#3C3489',cat:'academico',catL:'Normas académicas',
  title:'Normas Académicas Derecho -- Jornada Diurna (Plan DE04)',res:'07/2026',year:'2026',
  mat:'Aprueba Instructivo de Disposiciones Académicas Complementarias para la carrera de Derecho, jornada diurna, sedes Santiago y Coquimbo.',
  fecha:'Santiago, 10 de marzo de 2026',firm:'Rafael Pastor Besoain (Decano FACDEH)',
  txt:'Normas especiales de evaluación para el Plan DE04 de Derecho diurno (Res. 6214/2025), aplicable a estudiantes que ingresan en 2026.',
  pts:['Escala 1,0-7,0. Nota mínima aprobación: 4,0. Exigencia: 60%. Asistencia: 75%.','Nota mínima presentación a examen: 3,0. Eximición con nota de presentación ≥ 6,0.','Asignaturas disciplinares: 3 evaluaciones (30%+30%+40%). 3ª evaluación oral obligatoria en Derecho Civil, Procesal y Constitucional.','Ponderación: nota presentación 60% + examen final 40%.','Asignaturas electivas: sin examen. 2 evaluaciones (50%+50%).','Clínicas Jurídicas: 3 evaluaciones (60%+30%+10%). Sin eximición. Examen: 40% informe + 60% exposición oral.','Seminarios de Licenciatura: 20% asistencia (mínimo 80%) + 80% trabajos.','Examen de Licenciatura: en el 10° semestre, previa aprobación de todas las asignaturas.']},

nor08:{ico:'NOR',bg:'#EEEDFE',fg:'#3C3489',cat:'academico',catL:'Normas académicas',
  title:'Normas Académicas Derecho -- Jornada Vespertina (Plan DV03)',res:'08/2026',year:'2026',
  mat:'Aprueba Instructivo de Disposiciones Académicas Complementarias para la carrera de Derecho, jornada vespertina, sedes Santiago y Coquimbo.',
  fecha:'Santiago, 19 de marzo de 2026',firm:'Rafael Pastor Besoain (Decano FACDEH)',
  txt:'Normas especiales para el Plan DV03 de Derecho vespertino trimestral (Res. 6215/2025). Programación modular por asignatura en cada trimestre.',
  pts:['Escala 1,0-7,0. Nota mínima aprobación: 4,0. Exigencia: 60%.','Nota mínima presentación a examen: 3,0. Eximición con nota de presentación ≥ 6,0.','Programación modular trimestral: examen en fecha única por asignatura. Sin temporada especial ni de repetición.','Asignaturas disciplinares: 3 evaluaciones (30%+30%+40%). 3ª obligatoriamente oral en Derecho Civil, Procesal y Constitucional.','Ponderación: nota presentación 60% + examen fin de trimestre 40%.','Asignaturas electivas: sin examen. 2 evaluaciones (50%+50%).','Inasistencia: solo se permite recuperativa de la 1ª y 3ª evaluación con justificación.','Clínicas Jurídicas: sin eximición. Examen: 40% informe + 60% oral.','Examen de Licenciatura: en el 15° trimestre, previa aprobación de todas las asignaturas.']},

nor06:{ico:'NOR',bg:'#E1F5EE',fg:'#085041',cat:'academico',catL:'Normas académicas',
  title:'Normas Académicas Trabajo Social',res:'06/2026',year:'2026',
  mat:'Aprueba Instructivo de Disposiciones Académicas Complementarias para la carrera de Trabajo Social, sedes Santiago y Coquimbo.',
  fecha:'Santiago, 10 de marzo de 2026',firm:'Rafael Pastor Besoain (Decano FACDEH)',
  txt:'Normas especiales para el nuevo plan de Trabajo Social (Res. 5227/2024) vigente desde 2025, incluyendo reflexividad, práctica profesional y proceso de titulación.',
  pts:['Nota mínima de aprobación: 4,0. Nota mínima de presentación a examen: 4,0. Exigencia: 60%.','Asignaturas lectivas: 3 evaluaciones (30%+30%+40%). Asistencia mínima: 75%. Eximición con nota ≥ 5,5.','Línea de Reflexividad: sin examen. 3 evaluaciones (30%+30%+40%). Asistencia: 100% talleres y centros de práctica.','Práctica Profesional I y II: sin examen. 4 evaluaciones (25%+25%+25%+25%). Asistencia: 75% talleres, 100% centros.','Causales de reprobación inmediata en Reflexividad: 2 faltas injustificadas a pasantía; conductas contrarias a la ética; incumplimiento del reglamento interno.','Grado de Licenciatura: promedio asignaturas hasta 8°sem (70%) + Sistematización para la intervención (30%).','Título Profesional: promedio asignaturas hasta 10°sem sin Práctica I y II (70%) + promedio Práctica I y II (30%).','Comisión de examen: profesor guía + temático informante + profesor jornada (ministro de fe).']},

cur6214:{ico:'CUR',bg:'#E6F1FB',fg:'#0C447C',cat:'academico',catL:'Rediseño curricular',
  title:'Rediseño Curricular Derecho -- Jornada Diurna Semestral',res:'6214',year:'2025',
  mat:'Aprueba Rediseño Curricular del Plan de Estudios de la Carrera de Derecho Jornada Diurna y Régimen Semestral, a cargo de la Facultad de Derecho y Humanidades.',
  fecha:'Santiago, 03 de septiembre de 2025',
  firm:'Secretaría General · UCen (aprobado por Junta Directiva N°834, 01 julio 2025)',
  txt:'Nuevo plan de estudios DE04 para Derecho diurna semestral. Duración: 10 semestres. Grado: Licenciado/a en Derecho. El título de Abogado/a lo confiere la Corte Suprema.',
  pts:['Carrera creada en 1982; sede Coquimbo desde 2003.','Régimen semestral (18 semanas lectivas), presencial, jornada diurna en Santiago y Coquimbo.','10 semestres. Plan competitivo con ciclo inicial nivelador y formación práctica desde el primer año.','Incorpora Clínicas Jurídicas, seminarios de licenciatura y metodologías digitales.','Examen de Licenciatura en el 10° semestre previa aprobación de todas las asignaturas.','Aprobado unánimemente por Junta Directiva N°834 del 01 de julio de 2025.']},

cur6215:{ico:'CUR',bg:'#E6F1FB',fg:'#0C447C',cat:'academico',catL:'Rediseño curricular',
  title:'Rediseño Curricular Derecho -- Jornada Vespertina Trimestral',res:'6215',year:'2025',
  mat:'Aprueba Rediseño Curricular del Plan de Estudios de la Carrera de Derecho Jornada Vespertina y Régimen Trimestral, a cargo de la Facultad de Derecho y Humanidades.',
  fecha:'Santiago, 03 de septiembre de 2025',
  firm:'Secretaría General · UCen (aprobado por Junta Directiva N°834, 01 julio 2025)',
  txt:'Nuevo plan de estudios DV03 para Derecho vespertina trimestral. Duración: 15 trimestres. Grado: Licenciado/a en Derecho.',
  pts:['Régimen trimestral (13 semanas lectivas), presencial, jornada vespertina en Santiago y Coquimbo.','15 trimestres de duración. Programación modular: cada asignatura tiene cronograma propio.','Incorpora Clínicas Jurídicas, asignaturas electivas y seminarios de licenciatura.','Examen de Licenciatura en el 15° trimestre previa aprobación de todas las asignaturas.','Aprobado unánimemente por Junta Directiva N°834 del 01 de julio de 2025.']},

adm8090:{ico:'ADM',bg:'#E6F1FB',fg:'#0C447C',cat:'academico',catL:'Política académica',
  title:'Política de Admisión',res:'8090',year:'2025',
  mat:'Aprueba Política de Admisión de la Universidad Central de Chile.',
  fecha:'2025',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Marco que establece lineamientos transparentes para el ingreso a la UCEN en todos los segmentos y modalidades, garantizando igualdad de condiciones.',
  pts:['Define admisión como el proceso que permite el ingreso en cualquier segmento del Reglamento General de Estudios (Res. 9842).','Modalidades: Pregrado Regular, Continuidad, Postgrado, Educación Continua y otras que defina la UCEN.','Requisitos alineados con el Ministerio de Educación y el Sistema de Acceso a la Educación Superior.','Incorpora consideraciones que valoran la diversidad socioeconómica y demográfica.','Para pedagogías, los postulantes deben cumplir los requisitos de la Ley N°20.903.']},

mpe4946:{ico:'MPE',bg:'#EAF3DE',fg:'#27500A',cat:'academico',catL:'Modelo institucional',
  title:'Modelo de Progresión Estudiantil',res:'4946',year:'',
  mat:'Aprueba el Modelo de Progresión Estudiantil (MPE) de la Universidad Central de Chile.',
  fecha:'Universidad Central de Chile',firm:'Vicerrectoría Académica · Universidad Central de Chile',
  txt:'Sistema de seguimiento integral a la trayectoria académica estructurado en 4 dimensiones, articulando políticas de formación docente y acompañamiento estudiantil.',
  pts:['Dimensión 1 - Resultados: rendimiento académico, aprobación, retención, avance curricular y titulación oportuna.','Dimensión 2 - Curricular: diseño, metodologías y evaluación de planes de estudio.','Dimensión 3 - Enseñanza-aprendizaje: prácticas pedagógicas, formación docente, recursos didácticos y tecnologías.','Dimensión 4 - Acompañamiento: apoyo académico, psicoemocional, socioeconómico y psicoeducativo.','Las 4 dimensiones están presentes de manera transversal en los 4 ciclos formativos de la UCEN.']},

pei0092:{ico:'PEI',bg:'#E6F1FB',fg:'#0C447C',cat:'academico',catL:'Académico',
  title:'Homogeneización Horas y Créditos -- Cursos Sello / PEI',res:'0092',year:'2026',
  mat:'Aprueba homogeneizar la distribución de horas pedagógicas y créditos de los Cursos Sellos Institucionales, Formación Básica para la Vida Académica y Asignaturas Interdisciplinares en todos los planes de estudio vigentes.',
  fecha:'Santiago, 05 de enero de 2026',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Homogeneiza la carga horaria y crediticia de las asignaturas de formación general en todos los planes de estudio, facilitando el avance curricular y la gestión académica-administrativa.',
  pts:['Facilita que los estudiantes cursen asignaturas similares de formación general entre distintas carreras.','Introduce flexibilidad en la línea de formación general: Formación Básica, Cursos Sello e Interdisciplinares.','Permite desarrollar una oferta académica más amplia y sólida en estas asignaturas.','Facilita la gestión administrativa, registro y planeación en el sistema académico.','Alinea con los valores del nuevo PEC 2026-2032.','No afecta el total de créditos SCT transferibles ni los planes de estudio de los que son parte.']},

virt:{ico:'VIR',bg:'#E1F5EE',fg:'#085041',cat:'academico',catL:'Protocolo académico',
  title:'Proceso de Virtualización de Programas Académicos',res:'Protocolo',year:'2025',
  mat:'Protocolo para Facultades: Proceso de Virtualización de Programas Académicos. Dirección de Transformación Digital Educativa (DTDE), Vicerrectoría Académica.',
  fecha:'Abril 2025',firm:'Dirección de Transformación Digital Educativa (DTDE) · Vicerrectoría Académica',
  txt:'Marco procedimental que establece estándares de calidad, responsabilidades y plazos para la virtualización de programas académicos de la UCEN conforme a criterios CNA.',
  pts:['La DTDE (dependiente de la VRA) supervisa la virtualización bajo estándares CNA.','VRA: responsable de pregrado (Advance, vespertino, prosecuciones). VRIIP: responsable de magíster y doctorados.','Proceso en 3 etapas: (1) Antes de iniciar; (2) Desarrollo; (3) Finalización y validación.','Dedicación horaria del docente especialista: equivalente a horas totales del programa. Sin experiencia previa: +30% adicional.','Contrato de docente especialista: cede a la Universidad todos los derechos patrimoniales sobre recursos desarrollados.','La DTDE contacta a la Vicedecanatura para comunicar calendarios y presupuestos una vez aprobada la viabilidad.']},

res4029:{ico:'INT',bg:'#E6F1FB',fg:'#0C447C',cat:'academico',catL:'Internacionalización',
  title:'Modelo de Gestión Integral de la Internacionalización',res:'4029',year:'2025',
  mat:'Aprueba Modelo de Gestión Integral de la Internacionalización en la Universidad Central de Chile.',
  fecha:'Santiago, 14 de mayo de 2025',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Formaliza y consolida las instancias de gestión de la internacionalización, definiendo estructura, funciones y periodicidad de comités y consejos que coordinan esta función institucional.',
  pts:['Desde 1982, la UCEN ha generado alianzas estratégicas con IES internacionales.','La DRI diversificó su labor para abarcar formación, vinculación, investigación y docencia.','Define la estructura de gobernanza de la internacionalización a nivel institucional y de facultades.','Establece funciones, periodicidad y composición de los comités de internacionalización.','Articula la internacionalización del currículo como objetivo del PEC y el PEI.','Complementa el Procedimiento de Gestión de Convenios Internacionales (Res. 4538/2024).']},

inc3264:{ico:'INC',bg:'#EEEDFE',fg:'#3C3489',cat:'inclusion',catL:'Inclusión y diversidad',
  title:'Política de Inclusión y Diversidad',res:'3264',year:'2021',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba Política y Reglamento de Inclusión y Diversidad de la Universidad Central de Chile.',
  fecha:'Santiago, 07 de mayo de 2021',
  firm:'Neftalí Carabantes Hernández (Secretario General) · Santiago González Larraín (Rector)',
  txt:'Política sustentada en el enfoque de derechos que reconoce las diferencias de origen socioeconómico, culturales, étnicas, de orientación sexual e identidad de género, y discapacidad como valor transversal en la UCEN.',
  pts:['Crea la Unidad de Inclusión Estudiantil bajo la Vicerrectoría Académica.','Mecanismos de acceso especial para estudiantes con discapacidad o méritos afectados por discriminación.','Art. 11: seguimiento de egresados con apoyos y registro laboral.','Exige capacitación docente en adecuaciones curriculares y evaluación flexible.','Incorpora cursos sobre inclusión en los planes de estudio de pregrado.','Marco legal: Ley N°20.422 (discapacidad) y Ley N°20.609 (antidiscriminación).']},

res7470:{ico:'GEN',bg:'#FBEAF0',fg:'#72243E',cat:'inclusion',catL:'Género y convivencia',
  title:'Reglamento Acoso Sexual, Violencia de Género y Discriminación',res:'7470',year:'2025',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba Reglamento de Actuación ante Situaciones de Acoso Sexual, Violencia de Género y Discriminación de la Universidad Central de Chile.',
  fecha:'Santiago, 28 de octubre de 2025',
  firm:'Secretaría General · Santiago González Larraín (Rector) (aprobado por Junta Directiva N°844, 01 octubre 2025)',
  txt:'Reglamento integral que regula el acoso sexual, la violencia de género y la discriminación en el ámbito universitario. Unifica y actualiza todos los instrumentos anteriores con enfoque de género e interseccionalidad.',
  pts:['Aprobado unánimemente por Junta Directiva N°844 del 01 de octubre de 2025.','Integra y actualiza el Protocolo de Género (Res. 1129/2019), la Política Integral (Res. 5234/2022) y el Modelo de Prevención (Res. 5276/2022).','Promueve un entorno seguro y libre de violencia y discriminación para toda la comunidad universitaria.','Define conductas constitutivas de acoso sexual, violencia de género y discriminación.','Establece procedimientos de denuncia, investigación y sanción con garantía de debido proceso.','Aplica a toda la comunidad universitaria: estudiantes, académicos/as y funcionarios/as.']},

conv1156:{ico:'CON',bg:'#E1F5EE',fg:'#085041',cat:'inclusion',catL:'Convivencia',
  title:'Reglamento de Convivencia y Vida Estudiantil',res:'1156',year:'2020',
  mat:'Aprueba el Reglamento de Convivencia y Vida Estudiantil de la Universidad Central de Chile.',
  fecha:'2020',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Normas que regulan la convivencia, definen tipos de faltas y sus sanciones, y establecen los procedimientos de debido proceso en la comunidad universitaria.',
  pts:['Clasifica las faltas en leves, graves y gravísimas.','Sanciones faltas graves: prohibición de roles representativos; prohibición de ayudantías; pérdida de beneficios; reubicación de curso; suspensión hasta un semestre.','Sanciones faltas gravísimas: suspensión 1 a 2 semestres o expulsión definitiva.','Sanciones para personal administrativo y docente: conforme al Código del Trabajo y Ley de Acoso Sexual en Universidades.','Las sanciones más graves deben ser impuestas por Rectoría.','Establece el Tribunal de Convivencia y Vida Estudiantil como órgano resolutivo.']},

aud1101:{ico:'AUD',bg:'#FAEEDA',fg:'#633806',cat:'compliance',catL:'Auditoría',
  title:'Plan de Auditoría 2025',res:'1101',year:'2025',
  mat:'Aprueba el Plan de Auditoría 2025 de la Universidad Central de Chile.',
  fecha:'2025',firm:'Contraloría Universitaria · Universidad Central de Chile',
  txt:'Plan que establece las auditorías internas programadas para 2025, orientadas a verificar el cumplimiento normativo y la eficiencia de los procesos institucionales.',
  pts:['Define el alcance y objetivos de las auditorías internas para el período 2025.','Identifica unidades y procesos prioritarios a auditar.','Establece el cronograma de ejecución de auditorías.','Incluye metodología de evaluación y seguimiento de hallazgos.','Reporta resultados y recomendaciones a la Junta Directiva.']},

aud0920:{ico:'AUD',bg:'#FAEEDA',fg:'#633806',cat:'compliance',catL:'Auditoría',
  title:'Plan de Auditoría 2026 -- Contraloría Universitaria',res:'0920',year:'2026',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba Plan de Auditoría presentado por la Contraloría Universitaria para el año 2026 de la Universidad Central de Chile.',
  fecha:'Santiago, 20 de enero de 2026',
  firm:'Secretaría General · Santiago González Larraín (Rector) (aprobado por Junta Directiva N°854, 30 diciembre 2025)',
  txt:'Aprueba el Plan de Auditoría 2026 presentado por la Contraloría Universitaria y aprobado unánimemente por la Junta Directiva en sesión ordinaria N°854 del 30 de diciembre de 2025.',
  pts:['Promulga el Acuerdo N°3 de la Sesión Ordinaria N°854 de la Junta Directiva (30 diciembre 2025).','El Comité de Auditoría es un órgano de apoyo a la Junta Directiva y a la Rectoría.','El Plan fue aprobado previamente por el Comité de Auditoría en su Sesión Ordinaria N°27 del 30 de diciembre de 2025.','Establece las auditorías programadas para verificar cumplimiento normativo y correcta administración durante 2026.','Coordina con auditores internos y externos según corresponda.']},

com0921:{ico:'COM',bg:'#FAEEDA',fg:'#633806',cat:'compliance',catL:'Compliance',
  title:'Compliance Institucional',res:'0921',year:'',
  mat:'Aprueba el Programa de Compliance Institucional de la Universidad Central de Chile.',
  fecha:'Universidad Central de Chile',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Programa de cumplimiento normativo, ético y legal basado en la Ley N°20.393 sobre responsabilidad penal de personas jurídicas, aplicable a toda la comunidad universitaria.',
  pts:['Establece el modelo de prevención de delitos según Ley N°20.393.','Define el canal de denuncias y mecanismos de reporte para irregularidades.','Establece responsabilidades del Encargado de Prevención de Delitos.','Regula conflictos de interés, uso de recursos institucionales y conducta ética.','Incluye protocolos de auditoría interna y controles de cumplimiento.','Aplica a directivos, académicos y funcionarios de la UCEN.']},

res8576:{ico:'CNA',bg:'#EAF3DE',fg:'#27500A',cat:'compliance',catL:'Aseguramiento de calidad',
  title:'Reglamento de Autoevaluación Institucional -- DAC',res:'8576',year:'2024',
  mat:'Promulga acuerdo de la Junta Directiva que aprueba Reglamento de Autoevaluación Institucional de la Dirección de Aseguramiento de la Calidad de la Universidad Central de Chile.',
  fecha:'Santiago, 30 de diciembre de 2024',firm:'Secretaría General · Santiago González Larraín (Rector)',
  txt:'Marco normativo para el proceso de autoevaluación institucional bajo criterios y estándares de la Comisión Nacional de Acreditación (CNA), a cargo de la DAC a través del SIAC.',
  pts:['Entrega orientaciones generales de la DAC conforme al SIAC de la UCEN bajo estándares CNA.','Vincula con la Política de Calidad (Res. 9774/2023) y el SIAC (Res. 9775/2023).','Actualiza el procedimiento de autoevaluación de carreras (Res. 2468/2012) y la estructura de la DAC (Res. 4943/2016).','Define responsabilidades de la DAC, las unidades académicas y las instancias de revisión.','Establece el proceso para acreditación institucional y de carreras ante la CNA.']},

seg8082:{ico:'SEG',bg:'#FCEBEB',fg:'#791F1F',cat:'compliance',catL:'Seguridad TI',
  title:'Política de Seguridad de la Información',res:'8082',year:'',
  mat:'Aprueba Política de Seguridad de la Información de la Universidad Central de Chile.',
  fecha:'Universidad Central de Chile',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Marco que establece directrices para proteger la confidencialidad, integridad y disponibilidad de los activos de información de la UCEN, regulando el uso de sistemas, equipos y redes.',
  pts:['Protege la confidencialidad, integridad y disponibilidad de la información institucional.','Define responsabilidades de toda la comunidad universitaria respecto al manejo de información.','Incluye procedimientos de gestión de riesgos de seguridad de la información.','Regula el uso de sistemas de información, equipos tecnológicos y redes institucionales.','Establece protocolos ante incidentes de seguridad informática.']},

doc4949:{ico:'DOC',bg:'#EEEDFE',fg:'#3C3489',cat:'docencia',catL:'Formación docente',
  title:'Plan de Formación Docente',res:'4949',year:'',
  mat:'Aprueba el Plan de Formación Docente de la Universidad Central de Chile.',
  fecha:'Universidad Central de Chile',firm:'Vicerrectoría Académica · Universidad Central de Chile',
  txt:'Estrategia institucional de desarrollo pedagógico continuo para el cuerpo académico, orientada a fortalecer competencias en metodologías, evaluación y tecnologías educativas.',
  pts:['Define líneas de formación: didáctica, evaluación, tecnología educativa e investigación-acción.','Establece detección de necesidades formativas por unidad académica.','Coordina con la Dirección de Desarrollo Académico (DDA) la oferta de capacitaciones.','Vincula la formación docente con los indicadores del Convenio de Desempeño Docente (CDD).','Incluye formación en modalidades presencial, semipresencial y online.']},

doc5796:{ico:'I+I',bg:'#EEEDFE',fg:'#3C3489',cat:'docencia',catL:'Formación docente',
  title:'Plan de Formación, Innovación e Investigación en Docencia',res:'5796',year:'2025',
  mat:'Aprueba Plan de Formación, Innovación e Investigación en Docencia, a cargo de la Vicerrectoría Académica de la Universidad Central de Chile.',
  fecha:'Santiago, 12 de agosto de 2025',
  firm:'Secretaría General · UCen (solicitado por Directora DDA mediante Memorándum N°18/2025)',
  txt:'Plan institucional que integra formación, innovación e investigación en docencia bajo coordinación de la VRA, vinculado con el PEI y el PEC.',
  pts:['Aprobado a partir del Memorándum N°18/2025 de la Directora de Desarrollo Académico y opinión favorable del Vicerrector Académico.','Integra tres ejes: formación docente, innovación pedagógica e investigación en docencia.','Se alinea con el PEI (Res. 6244/2023) y el PEC 2021-2025 actualizado.','Incluye metodologías para el fomento de la innovación pedagógica y la investigación aplicada a la docencia.','Complementa y articula con el Plan de Formación Docente (Res. 4949).']},

res4488:{ico:'VCM',bg:'#E1F5EE',fg:'#085041',cat:'vcm',catL:'Vinculación con el Medio',
  title:'Sistema de Articulación para la VcM',res:'4488',year:'2025',
  mat:'Aprueba Sistema de Articulación para la Vinculación con el Medio en la Universidad Central de Chile.',
  fecha:'Santiago, 03 de junio de 2025',firm:'Secretaría General · Universidad Central de Chile',
  txt:'Formaliza y consolida las instancias de articulación de la VcM en la UCEN, integrándola como función transversal y estratégica a través de comités y consejos en distintos niveles de gestión.',
  pts:['Desde 2016, la UCEN ha implementado instancias de articulación para coordinar la VcM.','Consolida un modelo de gestión que integra la VcM como función transversal.','Responde a la Política de Vinculación con el Medio (Res. 5179/2024) y el PEI actualizado.','Define estructura, funciones, periodicidad y composición de los comités de VcM.','Coordina entre el Comité Asesor de Carrera, el Consejo de Egresados/as y las instancias de VcM.','Aplica a todos los niveles de gestión: institucional, de facultad y de carrera.']}
};

// -- LISTA DE DOCUMENTOS ------------------------------------------------------
var DOCS = [
  {k:'pec3142',   cat:'estrategico'},{k:'pgd3165',   cat:'estrategico'},
  {k:'calpgsem', cat:'calendario'}, {k:'calpgtri',  cat:'calendario'},
  {k:'calpregsem',cat:'calendario'},{k:'calpregtri',cat:'calendario'},
  {k:'calvriip', cat:'calendario'},
  {k:'rge9842',  cat:'academico'},  {k:'nor07',     cat:'academico'},
  {k:'nor08',    cat:'academico'},  {k:'nor06',     cat:'academico'},
  {k:'cur6214',  cat:'academico'},  {k:'cur6215',   cat:'academico'},
  {k:'adm8090',  cat:'academico'},  {k:'mpe4946',   cat:'academico'},
  {k:'pei0092',  cat:'academico'},  {k:'virt',      cat:'academico'},
  {k:'res4029',  cat:'academico'},
  {k:'inc3264',  cat:'inclusion'},  {k:'res7470',   cat:'inclusion'},
  {k:'conv1156', cat:'inclusion'},
  {k:'aud1101',  cat:'compliance'}, {k:'aud0920',   cat:'compliance'},
  {k:'com0921',  cat:'compliance'}, {k:'res8576',   cat:'compliance'},
  {k:'seg8082',  cat:'compliance'},
  {k:'doc4949',  cat:'docencia'},   {k:'doc5796',   cat:'docencia'},
  {k:'res4488',  cat:'vcm'}
];

// -- ÁREAS NORMATIVA ----------------------------------------------------------
var AREAS = [
  {t:'Planificación estratégica', c:'#0057a8',
   r:[['pec3142','Plan Estratégico Corporativo 2026-2032','Res. 3142 · 2026'],
      ['pgd3165','Políticas Globales de Desarrollo','Res. 3165']]},
  {t:'Reglamentos y normas de carrera FACDEH', c:'#534AB7',
   r:[['rge9842','Reglamento General de Estudios de Pregrado','Res. 9842 · 2023'],
      ['nor07','Normas Académicas Derecho -- jornada diurna','Res. 07/2026'],
      ['nor08','Normas Académicas Derecho -- jornada vespertina','Res. 08/2026'],
      ['nor06','Normas Académicas Trabajo Social','Res. 06/2026']]},
  {t:'Planes de estudio -- Carrera de Derecho', c:'#3C3489',
   r:[['cur6214','Rediseño curricular Derecho diurno semestral','Res. 6214 · 2025'],
      ['cur6215','Rediseño curricular Derecho vespertino trimestral','Res. 6215 · 2025']]},
  {t:'Calendarios 2026', c:'#0057a8',
   r:[['calpregsem','Pregrado semestral -- Stgo & Coquimbo','Res. 0040 · 2026'],
      ['calpregtri','Pregrado trimestral -- Advance & Vespertino','Res. 0041 · 2026'],
      ['calpgsem','Postgrado semestral -- Santiago','Res. 0036 · 2026'],
      ['calpgtri','Postgrado trimestral -- Santiago','Res. 0039 · 2026'],
      ['calvriip','Concursos Internos 2026 -- VRIIP','VRIIP · 2026']]},
  {t:'Políticas académicas institucionales', c:'#639922',
   r:[['adm8090','Política de Admisión','Res. 8090 · 2025'],
      ['mpe4946','Modelo de Progresión Estudiantil','Res. 4946'],
      ['pei0092','Homogeneización Cursos Sello / PEI','Res. 0092 · 2026'],
      ['virt','Proceso de Virtualización de Programas','Protocolo 2025'],
      ['res4029','Modelo de Gestión Integral de la Internacionalización','Res. 4029 · 2025']]},
  {t:'Inclusión, género y convivencia', c:'#D4537E',
   r:[['inc3264','Política de Inclusión y Diversidad','Res. 3264 · 2021'],
      ['res7470','Reglamento Acoso Sexual y Violencia de Género','Res. 7470 · 2025'],
      ['conv1156','Reglamento de Convivencia y Vida Estudiantil','Res. 1156 · 2020']]},
  {t:'Compliance, auditoría y calidad', c:'#BA7517',
   r:[['aud1101','Plan de Auditoría 2025','Res. 1101 · 2025'],
      ['aud0920','Plan de Auditoría 2026 -- Contraloría Universitaria','Res. 0920 · 2026'],
      ['com0921','Compliance Institucional','Res. 0921'],
      ['res8576','Reglamento de Autoevaluación Institucional -- DAC','Res. 8576 · 2024'],
      ['seg8082','Política de Seguridad de la Información','Res. 8082']]},
  {t:'Docencia y formación académica', c:'#3C3489',
   r:[['doc4949','Plan de Formación Docente','Res. 4949'],
      ['doc5796','Plan de Formación, Innovación e Investigación en Docencia','Res. 5796 · 2025']]},
  {t:'Vinculación con el Medio', c:'#0F6E56',
   r:[['res4488','Sistema de Articulación para la VcM','Res. 4488 · 2025']]}
];

var POLITICAS = ['pec3142','adm8090','inc3264','res7470','com0921','seg8082','doc4949','mpe4946','conv1156','pgd3165'];
var CALKEYS   = ['calpregsem','calpregtri','calpgsem','calpgtri','calvriip'];
var AREAS_HOME = [
  ['#0057a8','Calendarios 2026','5 docs'],
  ['#534AB7','Académico / Reglamentos','10 docs'],
  ['#639922','Inclusión y Género','3 docs'],
  ['#BA7517','Compliance y Auditoría','5 docs'],
  ['#993C1D','Seguridad TI','1 doc'],
  ['#3C3489','Docencia y Formación','2 docs'],
  ['#0F6E56','Vinculación con el Medio','1 doc'],
  ['#0057a8','Internacionalización','1 doc'],
  ['#888780','Planificación Estratégica','2 docs']
];

var af = 'todos';

// -- MODAL --------------------------------------------------------------------
function openDoc(k) {
  var d = DB[k]; if (!d) return;
  document.getElementById('m-ico').style.background = d.bg;
  document.getElementById('m-ico').style.color = d.fg;
  document.getElementById('m-ico').textContent = d.ico;
  document.getElementById('m-badge').textContent = d.catL;
  document.getElementById('m-badge').style.background = d.bg;
  document.getElementById('m-badge').style.color = d.fg;
  document.getElementById('m-res').textContent = 'Res. ' + d.res + (d.year ? ' · ' + d.year : '');
  document.getElementById('m-title').textContent = d.title;
  document.getElementById('m-mat').textContent = d.mat;
  document.getElementById('m-fecha').textContent = d.fecha;
  document.getElementById('m-firm').textContent = d.firm;
  document.getElementById('m-txt').textContent = d.txt;
  document.getElementById('m-pts').innerHTML = d.pts.map(function(p){return '<li>'+p+'</li>';}).join('');
  document.getElementById('mbg').classList.add('on');
}
function closeModal() { document.getElementById('mbg').classList.remove('on'); }

// -- RENDERIZADO --------------------------------------------------------------
function renderDocs() {
  var q = (document.getElementById('srch').value || '').toLowerCase();
  var list = DOCS.filter(function(d){
    if (af !== 'todos' && d.cat !== af) return false;
    if (!q) return true;
    var db = DB[d.k];
    return db && (db.title.toLowerCase().indexOf(q) >= 0 || db.res.toLowerCase().indexOf(q) >= 0 || db.mat.toLowerCase().indexOf(q) >= 0);
  });
  var el = document.getElementById('dl');
  if (!list.length) { el.innerHTML = '<div style="padding:1.5rem;text-align:center;color:var(--t3);font-size:13px">Sin resultados</div>'; return; }
  el.innerHTML = list.map(function(d){
    var db = DB[d.k]; if (!db) return '';
    return '<div class="dr" onclick="openDoc(\''+d.k+'\')">'
      +'<div class="ib" style="background:'+db.bg+';color:'+db.fg+'">'+db.ico+'</div>'
      +'<div style="flex:1;min-width:0"><div style="font-size:13px;font-weight:500;color:var(--txt);white-space:nowrap;overflow:hidden;text-overflow:ellipsis">'+db.title+'</div>'
      +'<div style="font-size:11.5px;color:var(--t3)">Res. '+db.res+(db.year?' · '+db.year:'')+'</div></div>'
      +'<span class="bv">Ver ficha &#8594;</span></div>';
  }).join('');
}
function setF(cat, btn) {
  af = cat;
  document.querySelectorAll('.pill').forEach(function(p){p.classList.remove('on');});
  btn.classList.add('on');
  renderDocs();
}

function renderPoliticas() {
  var el = document.getElementById('pgrid');
  el.innerHTML = POLITICAS.map(function(k){
    var d = DB[k]; if (!d) return '';
    return '<div class="pcard" onclick="openDoc(\''+k+\')">'
      +'<div style="display:flex;align-items:center;gap:9px;margin-bottom:8px">'
      +'<div style="width:8px;height:8px;border-radius:50%;background:'+d.fg+';flex-shrink:0"></div>'
      +'<span style="font-size:13px;font-weight:500;color:var(--txt)">'+d.title+'</span></div>'
      +'<p style="font-size:12px;color:var(--t2);line-height:1.5">'+d.txt.substring(0,120)+'&#8230;</p>'
      +'<div style="font-size:11px;color:var(--t3);margin-top:8px">Res. '+d.res+(d.year?' · '+d.year:'')+'</div></div>';
  }).join('');
}

function renderNormativa() {
  var el = document.getElementById('norm');
  el.innerHTML = AREAS.map(function(a){
    return '<div class="na">'
      +'<div class="na-hd"><div style="width:3px;height:15px;border-radius:2px;background:'+a.c+';flex-shrink:0"></div>'
      +'<span style="font-size:13px;font-weight:500;color:var(--txt)">'+a.t+'</span></div>'
      +'<div class="nt"><div class="nth"><span>Documento</span><span>Resolución</span><span>Estado</span></div>'
      +a.r.map(function(r){
        return '<div class="nr" onclick="openDoc(\''+r[0]+'\')"><span style="color:var(--txt)">'+r[1]+'</span>'
          +'<span style="color:var(--t3)">'+r[2]+'</span>'
          +'<span class="bv">Ver &#8594;</span></div>';
      }).join('')+'</div></div>';
  }).join('');
}

function renderCalendarios() {
  var el = document.getElementById('cgrid');
  el.innerHTML = CALKEYS.map(function(k){
    var d = DB[k]; if (!d) return '';
    return '<div class="pcard" onclick="openDoc(\''+k+\')">'
      +'<div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:8px">'
      +'<span style="font-size:13px;font-weight:500;color:var(--txt)">'+d.title+'</span>'
      +'<span style="font-size:10px;padding:3px 8px;background:'+d.bg+';color:'+d.fg+';border-radius:20px">Res. '+d.res+'</span></div>'
      +'<div style="display:flex;flex-direction:column;gap:4px">'
      +d.pts.slice(0,4).map(function(p){return '<div style="font-size:11.5px;color:var(--t2)">'+p+'</div>';}).join('')
      +'</div><div style="font-size:11px;color:var(--t3);margin-top:8px">Ver todas las fechas &#8594;</div></div>';
  }).join('');
}

function renderAreas() {
  var el = document.getElementById('areas-list');
  el.innerHTML = AREAS_HOME.map(function(a){
    return '<div style="display:flex;align-items:center;justify-content:space-between;padding:7px 0;border-bottom:.5px solid var(--bd)">'
      +'<div style="display:flex;align-items:center;gap:8px"><div style="width:6px;height:6px;border-radius:50%;background:'+a[0]+';flex-shrink:0"></div>'
      +'<span style="font-size:12.5px;color:var(--txt)">'+a[1]+'</span></div>'
      +'<span style="font-size:11.5px;color:var(--t2);background:var(--bg2);padding:2px 8px;border-radius:20px">'+a[2]+'</span></div>';
  }).join('');
}

// -- NAVEGACIÓN ---------------------------------------------------------------
function nav(page) {
  document.querySelectorAll('.pg').forEach(function(p){p.classList.remove('on');});
  document.getElementById('pg-'+page).classList.add('on');
  document.querySelectorAll('.nb').forEach(function(b){b.classList.remove('on');});
  var nb = document.getElementById('nb-'+page);
  if (nb) nb.classList.add('on');
  if (page === 'resoluciones') renderDocs();
  document.getElementById('main').scrollTop = 0;
}

// -- INICIO -------------------------------------------------------------------
renderAreas();
renderPoliticas();
renderNormativa();
renderCalendarios();
</script>
</body>
</html>
