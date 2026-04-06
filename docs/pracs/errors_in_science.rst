==========================================
Types of Errors in Scientific Experiments
==========================================

*Understanding error types helps evaluate the accuracy, precision, and
validity of experimental results.*

This resource uses a **two-level model**:

* **Primary classification (assessment level):**
  :P:`Systematic errors`, :R:`Random errors`, and :O:`Personal errors`
* **Secondary classification (explanation level):**
  Instrumental, observational/procedural, method limitation, or environmental sources

----

How to Analyse Any Error: A Four-Step Framework
------------------------------------------------

Use this framework whenever you are asked to identify, explain, or evaluate
sources of error.

**Step 1 — Identify the source** *(what caused it?)*

* **Instrument** — :P:`zero error`, :P:`calibration fault`, :R:`resolution limit`
* **Observation / procedure** — :P:`parallax`, :R:`technique variation`,
  :O:`operator error`, :O:`recording mistake`
* **Method** — :P:`design flaw`, :P:`built-in assumption`
* **Environment (variation)** — :R:`temperature fluctuation`, :R:`vibration`,
  :R:`lighting variation`
* **Environment (bias)** — :P:`consistently elevated temperature`,
  :P:`persistent interference`, :P:`constant lighting offset`

.. list-table::
    :header-rows: 1
    :widths: 22 26 26 26

    * - Source
      - :P:`Systematic`
      - :R:`Random`
      - :O:`Personal`
    * - **Instrument**
      - :P:`zero error`, :P:`calibration fault`
      - :R:`resolution limit`
      -
    * - **Observation / Procedure**
      - :P:`parallax`
      - :R:`technique variation`
      - :O:`operator error`, :O:`recording mistake`
    * - **Method Limitation**
      - :P:`design flaw`, :P:`built-in assumption`
      -
      -
    * - **Environment (variation)**
      -
      - :R:`temperature fluctuation`, :R:`vibration`, :R:`lighting variation`
      -
    * - **Environment (bias)**
      - :P:`consistently elevated temperature`, :P:`persistent interference`,
        :P:`constant lighting offset`
      -
      -


**Step 2 — Classify the behaviour** *(how does it affect the data?)*

* Consistent, one-direction shift → :P:`Systematic error` → affects accuracy
* Unpredictable spread → :R:`Random error` → affects precision
* One-off mistake → :O:`Personal error` → discard and repeat

**Step 3 — Explain the impact**

* :P:`Systematic:` all results shifted consistently too high or too low
* :R:`Random:` results scattered around the true value
* :O:`Personal:` isolated invalid result; not representative

**Step 4 — Suggest an improvement**

* :P:`Systematic` → eliminate the source (recalibrate, redesign, correct setup)
* :R:`Random` → repeat and average; increase sample size
* :O:`Personal` → repeat the measurement correctly

----

Quick Reference: Mapping Source to Classification
------------------------------------------------------

.. list-table::
    :header-rows: 1
    :widths: 32 16 16 36

    * - Error
      - Source Category
      - Classification
      - Fix / Reduce by…
    * - :P:`Zero error`
      - Instrumental
      - :P:`Systematic`
      - :P:`Zero instrument before use`
    * - :P:`Calibration error`
      - Instrumental
      - :P:`Systematic`
      - :P:`Verify or recalibrate equipment`
    * - :R:`Resolution limitation`
      - Instrumental
      - :R:`Random`
      - :R:`Higher-resolution instrument`
    * - :P:`Parallax error`
      - Observational
      - :P:`Systematic`
      - :P:`Read scale at eye level`
    * - :O:`Operator / technique error`
      - Observational
      - :O:`Personal`
      - :O:`Follow procedure; repeat trial`
    * - :P:`Method limitation`
      - Method
      - :P:`Systematic`
      - :P:`Redesign experiment`
    * - :O:`Recording error`
      - Observational
      - :O:`Personal`
      - :O:`Check and re-read data`
    * - :P:`Temperature variation` / :R:`fluctuation`
      - Environmental
      - :P:`Systematic` / :R:`Random`
      - :P:`Control` or :R:`monitor conditions`
    * - :R:`Vibration / interference`
      - Environmental
      - :R:`Random`
      - :R:`Isolate apparatus`
    * - :P:`Lighting bias` / :R:`lighting variation`
      - Environmental
      - :P:`Systematic` / :R:`Random`
      - :P:`Correct` or :R:`shield light source`