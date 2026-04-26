===================================
Earth: Adding circumstances
===================================

| A **circumstance** is an adverbial phrase that adds context to a clause —
| expressing *when* or *where* something happens.
|
| Unlike qualifiers (which are embedded inside a noun group and cannot move),
| circumstances are **mobile**: the same phrase can sit at the end of a clause
| *or* be shifted to the front — and the grammar still works.
| This is the key test that separates circumstances from qualifiers.

----

Types of circumstance
---------------------

- **Time** (when?) — *over long periods*, *during earthquakes*
- **Place** (where?) — *along active fault zones*, *at mid-ocean ridges*

----

Example: The mobility test
---------------------------

| Simple clause: Water erodes weakened rock.
|
| **End position:** Water erodes weakened rock **over long periods**.
| **Front position:** **Over long periods**, water erodes weakened rock.
|
| Both are grammatical. The phrase is not locked inside a noun — it is a circumstance.

----

.. admonition:: Drag and drop — Circumstances
    :class: cloze

    | For each clause, drag the correct circumstance into **both** gaps:
    | once at the **end** of the clause, and once at the **front**.
    | This shows that the phrase is mobile and is not embedded in a noun group.

    .. raw:: html

        <div id="circumstances-app" style="margin-top:1.2rem;">

          <div id="phrase-bank" style="margin-bottom:1.4rem;">
            <div style="font-size:0.75rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;color:#64748b;margin-bottom:0.6rem;font-family:sans-serif;">Phrase bank — drag to the gaps</div>
            <div id="chips" style="display:flex;flex-wrap:wrap;gap:8px;"></div>
          </div>

          <div id="exercises"></div>

          <div style="margin-top:1.2rem;display:flex;align-items:center;gap:12px;flex-wrap:wrap;">
            <button id="btn-check" onclick="checkAnswers()" style="padding:8px 20px;border-radius:7px;border:none;background:#4F46E5;color:#fff;font-size:14px;font-family:sans-serif;font-weight:600;cursor:pointer;">Check answers</button>
            <button onclick="resetAll()" style="padding:8px 20px;border-radius:7px;border:1.5px solid #e2e8f0;background:transparent;color:#475569;font-size:14px;font-family:sans-serif;font-weight:600;cursor:pointer;">Reset</button>
            <span id="score-display" style="display:none;font-family:sans-serif;font-size:14px;font-weight:600;padding:6px 14px;border-radius:7px;"></span>
          </div>
          <p style="font-size:12px;font-family:sans-serif;color:#94a3b8;margin-top:0.5rem;">Click a placed phrase to remove it.</p>
        </div>

        <script>
        (function() {

          var PHRASES = [
            { id:"p1", text:"along active fault zones",       type:"place" },
            { id:"p2", text:"at convergent boundaries",       type:"place" },
            { id:"p3", text:"at mid-ocean ridges",            type:"place" },
            { id:"p4", text:"beneath volcanic regions",       type:"place" },
            { id:"p5", text:"during earthquakes",             type:"time"  },
            { id:"p6", text:"during major seismic events",    type:"time"  },
            { id:"p7", text:"during seismic rupture",         type:"time"  },
            { id:"p8", text:"over long periods",              type:"time"  },
          ];

          var EXERCISES = [
            { id:1, clause:"Water erodes weakened rock",         front:"water erodes weakened rock",                    answer:"p8", type:"time"  },
            { id:2, clause:"Stress fractures the crust",         front:"stress fractures the crust",                    answer:"p1", type:"place" },
            { id:3, clause:"Subduction destroys oceanic crust",  front:"subduction destroys oceanic crust",             answer:"p2", type:"place" },
            { id:4, clause:"Heat weakens the crust",             front:"heat weakens the crust",                        answer:"p4", type:"place" },
            { id:5, clause:"Strong building design reduces earthquake damage", front:"strong building design reduces earthquake damage", answer:"p6", type:"time"  },
            { id:6, clause:"Seismometers detect ground movement", front:"seismometers detect ground movement",          answer:"p5", type:"time"  },
            { id:7, clause:"Magma creates new oceanic crust",    front:"magma creates new oceanic crust",               answer:"p3", type:"place" },
            { id:8, clause:"Plates compress the crust",          front:"plates compress the crust",                     answer:"p2", type:"place" },
            { id:9, clause:"Plates slip along faults",           front:"plates slip along faults",                      answer:"p7", type:"time"  },
          ];

          var TYPE_STYLE = {
            time:  { bg:"#FEF3C7", border:"#F59E0B", text:"#78350F" },
            place: { bg:"#D1FAE5", border:"#34D399", text:"#064E3B" },
          };

          /* state */
          var drops = {};   /* key: exId+"-"+pos  value: phraseId */
          var checked = false;
          var dragging = null;

          function getUsedCounts() {
            var c = {};
            Object.values(drops).forEach(function(id){ c[id] = (c[id]||0)+1; });
            return c;
          }

          /* ---- render chip ---- */
          function makeChip(phrase, ghost) {
            var s = TYPE_STYLE[phrase.type];
            var div = document.createElement("div");
            div.setAttribute("draggable", "true");
            div.dataset.id = phrase.id;
            div.style.cssText = "display:inline-flex;align-items:center;padding:5px 14px;border-radius:24px;border:1.5px solid "+s.border+";background:"+s.bg+";color:"+s.text+";font-size:13px;font-style:italic;font-family:Georgia,serif;font-weight:500;cursor:grab;user-select:none;transition:opacity 0.2s;"+(ghost?"opacity:0.35;cursor:default;":"");
            div.textContent = phrase.text;
            div.addEventListener("dragstart", function(e){
              if(ghost){ e.preventDefault(); return; }
              dragging = phrase.id;
              e.dataTransfer.effectAllowed = "move";
            });
            return div;
          }

          /* ---- render slot ---- */
          function makeSlot(exId, pos) {
            var key = exId+"-"+pos;
            var phraseId = drops[key];
            var phrase = phraseId ? PHRASES.find(function(p){return p.id===phraseId;}) : null;

            var span = document.createElement("span");
            span.dataset.key = key;

            var correct = null;
            if(checked && phrase){
              var ex = EXERCISES.find(function(e){return e.id===exId;});
              correct = phraseId === ex.answer;
            }

            var border, bg, color;
            if(correct===true){  border="#10B981"; bg="#D1FAE5"; color="#065F46"; }
            else if(correct===false){ border="#EF4444"; bg="#FEE2E2"; color="#991B1B"; }
            else if(phrase){     border="#6366F1"; bg="#EEF2FF"; color="#4338CA"; }
            else{                border="#CBD5E1"; bg="#F8FAFC"; color="#94A3B8"; }

            var borderStyle = phrase ? "1.5px solid" : "2px dashed";
            span.style.cssText = "display:inline-flex;align-items:center;min-width:"+(phrase?"auto":"160px")+";height:30px;border-radius:6px;border:"+borderStyle+" "+border+";background:"+bg+";padding:0 10px;cursor:"+(phrase?"pointer":"default")+";vertical-align:middle;transition:all 0.15s;";

            if(phrase){
              span.innerHTML = "<span style='font-size:13px;font-style:italic;font-family:Georgia,serif;font-weight:500;color:"+color+";white-space:nowrap;'>"+phrase.text+(correct===true?" ✓":correct===false?" ✗":"")+"</span>";
              span.title = "Click to remove";
              span.addEventListener("click", function(){
                delete drops[key];
                checked = false;
                render();
              });
            } else {
              span.innerHTML = "<span style='font-size:12px;font-family:sans-serif;color:#94A3B8;'>drop here</span>";
              span.addEventListener("dragover", function(e){
                e.preventDefault();
                span.style.border = "2px dashed #6366F1";
                span.style.background = "#EEF2FF";
              });
              span.addEventListener("dragleave", function(){
                span.style.border = "2px dashed #CBD5E1";
                span.style.background = "#F8FAFC";
              });
              span.addEventListener("drop", function(e){
                e.preventDefault();
                if(!dragging) return;
                drops[key] = dragging;
                dragging = null;
                checked = false;
                render();
              });
            }
            return span;
          }

          /* ---- render badge ---- */
          function makeBadge(type){
            var s = TYPE_STYLE[type];
            var b = document.createElement("span");
            b.style.cssText = "font-size:11px;font-weight:600;letter-spacing:0.04em;padding:2px 8px;border-radius:20px;background:"+s.bg+";color:"+s.text+";border:1px solid "+s.border+";text-transform:uppercase;font-family:sans-serif;white-space:nowrap;margin-left:8px;";
            b.textContent = type;
            return b;
          }

          /* ---- main render ---- */
          function render(){
            var used = getUsedCounts();

            /* phrase bank */
            var chipsEl = document.getElementById("chips");
            chipsEl.innerHTML = "";
            PHRASES.forEach(function(p){
              /* how many exercises need this phrase */
              var needed = EXERCISES.filter(function(ex){return ex.answer===p.id;}).length;
              /* each exercise needs it twice (end + front) */
              var maxUses = needed * 2;
              var timesUsed = used[p.id] || 0;
              var ghost = timesUsed >= maxUses;
              chipsEl.appendChild(makeChip(p, ghost));
            });

            /* exercises */
            var exEl = document.getElementById("exercises");
            exEl.innerHTML = "";
            EXERCISES.forEach(function(ex, i){
              var wrap = document.createElement("div");
              wrap.style.cssText = "padding:1rem 0;"+(i<EXERCISES.length-1?"border-bottom:1px solid #F1F5F9;":"");

              /* header row */
              var header = document.createElement("div");
              header.style.cssText = "display:flex;align-items:center;gap:8px;margin-bottom:10px;";

              var num = document.createElement("span");
              num.style.cssText = "width:24px;height:24px;border-radius:50%;background:#EEF2FF;color:#4338CA;font-size:12px;font-family:sans-serif;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;";
              num.textContent = ex.id;

              var simple = document.createElement("span");
              simple.style.cssText = "font-size:13px;font-family:sans-serif;color:#64748B;font-style:italic;";
              simple.textContent = ex.clause+".";

              header.appendChild(num);
              header.appendChild(simple);
              header.appendChild(makeBadge(ex.type));
              wrap.appendChild(header);

              /* end row */
              var endRow = document.createElement("div");
              endRow.style.cssText = "margin-bottom:8px;padding-left:34px;font-size:14px;color:#334155;line-height:2;";

              var endLabel = document.createElement("span");
              endLabel.style.cssText = "font-size:11px;font-family:sans-serif;color:#94A3B8;font-weight:600;text-transform:uppercase;letter-spacing:0.08em;margin-right:10px;";
              endLabel.textContent = "end →";

              endRow.appendChild(endLabel);
              endRow.appendChild(document.createTextNode(ex.clause+" "));
              endRow.appendChild(makeSlot(ex.id, "end"));
              endRow.appendChild(document.createTextNode("."));
              wrap.appendChild(endRow);

              /* front row */
              var frontRow = document.createElement("div");
              frontRow.style.cssText = "padding-left:34px;font-size:14px;color:#334155;line-height:2;";

              var frontLabel = document.createElement("span");
              frontLabel.style.cssText = "font-size:11px;font-family:sans-serif;color:#94A3B8;font-weight:600;text-transform:uppercase;letter-spacing:0.08em;margin-right:10px;";
              frontLabel.textContent = "front →";

              frontRow.appendChild(frontLabel);
              frontRow.appendChild(makeSlot(ex.id, "front"));
              frontRow.appendChild(document.createTextNode(", "+ex.front+"."));
              wrap.appendChild(frontRow);

              exEl.appendChild(wrap);
            });

            /* check button state */
            var allFilled = EXERCISES.every(function(ex){
              return drops[ex.id+"-end"] && drops[ex.id+"-front"];
            });
            var btn = document.getElementById("btn-check");
            btn.disabled = !allFilled || checked;
            btn.style.background = (allFilled && !checked) ? "#4F46E5" : "#E2E8F0";
            btn.style.color = (allFilled && !checked) ? "#fff" : "#94A3B8";
            btn.style.cursor = (allFilled && !checked) ? "pointer" : "default";
          }

          window.checkAnswers = function(){
            checked = true;
            var score = EXERCISES.filter(function(ex){
              return drops[ex.id+"-end"]===ex.answer && drops[ex.id+"-front"]===ex.answer;
            }).length;
            render();
            var sd = document.getElementById("score-display");
            sd.style.display = "inline-block";
            sd.textContent = score+"/"+EXERCISES.length+" correct";
            sd.style.background = score===EXERCISES.length ? "#D1FAE5" : "#FEF3C7";
            sd.style.color = score===EXERCISES.length ? "#065F46" : "#92400E";
          };

          window.resetAll = function(){
            drops = {};
            checked = false;
            document.getElementById("score-display").style.display = "none";
            render();
          };

          render();

        })();
        </script>

    .. dropdown:: Reveal answer key
        :icon: check-circle
        :class-container: dropdown-cloze

        .. tab-set::

            .. tab-item:: Model answers

                .. list-table::
                    :header-rows: 1
                    :widths: 5 10 40 40

                    * - #
                      - Type
                      - End position
                      - Front position
                    * - 1.
                      - time
                      - Water erodes weakened rock **over long periods**.
                      - **Over long periods**, water erodes weakened rock.
                    * - 2.
                      - place
                      - Stress fractures the crust **along active fault zones**.
                      - **Along active fault zones**, stress fractures the crust.
                    * - 3.
                      - place
                      - Subduction destroys oceanic crust **at convergent boundaries**.
                      - **At convergent boundaries**, subduction destroys oceanic crust.
                    * - 4.
                      - place
                      - Heat weakens the crust **beneath volcanic regions**.
                      - **Beneath volcanic regions**, heat weakens the crust.
                    * - 5.
                      - time
                      - Strong building design reduces earthquake damage **during major seismic events**.
                      - **During major seismic events**, strong building design reduces earthquake damage.
                    * - 6.
                      - time
                      - Seismometers detect ground movement **during earthquakes**.
                      - **During earthquakes**, seismometers detect ground movement.
                    * - 7.
                      - place
                      - Magma creates new oceanic crust **at mid-ocean ridges**.
                      - **At mid-ocean ridges**, magma creates new oceanic crust.
                    * - 8.
                      - place
                      - Plates compress the crust **at convergent boundaries**.
                      - **At convergent boundaries**, plates compress the crust.
                    * - 9.
                      - time
                      - Plates slip along faults **during seismic rupture**.
                      - **During seismic rupture**, plates slip along faults.
