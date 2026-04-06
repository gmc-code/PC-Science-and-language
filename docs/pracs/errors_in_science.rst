==========================================
Types of Errors in Scientific Experiments
==========================================

*Understanding error types helps evaluate the accuracy, precision, and
validity of experimental results.*

This resource uses a **two-level model**:

* **Primary classification (assessment level):**
  :P:`Systematic errors`, :R:`Random errors`, and :O:`Personal errors`
* **Secondary classification (explanation level):**
  Instrumental, observational/procedural, method, or environmental sources

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
    * - **Method**
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
    * - Zero error
      - Instrumental
      - Systematic
      - Zero instrument before use
    * - Calibration error
      - Instrumental
      - Systematic
      - Verify or recalibrate equipment
    * - Resolution limitation
      - Instrumental
      - Random
      - Higher-resolution instrument
    * - Parallax error
      - Observational
      - Systematic
      - Read scale at eye level
    * - Operator / technique error
      - Observational
      - Personal
      - Follow procedure; repeat trial
    * - Method limitation
      - Method
      - Systematic
      - Redesign experiment
    * - Recording error
      - Observational
      - Personal
      - Check and re-read data
    * - Temperature variation
      - Environmental
      - Random or Systematic
      - Control or monitor conditions
    * - Vibration / interference
      - Environmental
      - Random
      - Isolate apparatus
    * - Lighting conditions
      - Environmental
      - Random or Systematic
      - Ensure consistent lighting

----

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
    * - **Method**
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
