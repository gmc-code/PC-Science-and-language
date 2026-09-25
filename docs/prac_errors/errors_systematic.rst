==========================================
Systematic Errors
==========================================

*Systematic errors cause a consistent bias in all measurements.*

Key features
----------------

* Results are consistently too high or too low
* Repetition does **not** reduce the error
* Accuracy is reduced


----

.. grid:: 12
    :gutter: 0

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_zero.svg
            :width: 100%

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_calibration.svg
            :width: 100%


.. grid:: 12
    :gutter: 0

    .. grid-item::
        :columns: 3

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_parallax.svg
            :width: 100%

    .. grid-item::
        :columns: 3

.. grid:: 12
    :gutter: 0

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_parallax.svg
            :width: 100%

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_parallax_full.svg
            :width: 100%


.. grid:: 12
    :gutter: 0

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_method_limitation.svg
            :width: 100%

    .. grid-item::
        :columns: 6

        .. image:: images/systematic_error_environmental.svg
            :width: 100%


----

Common systematic errors
------------------------------------

.. list-table::
    :header-rows: 1
    :widths: 16 16 34 34

    * - Source
      - Error Type
      - Explanation
      - Fix / Reduce by…
    * - Instrumental
      - Zero error
      - Instrument does not read zero, shifting all values.
      - Zero or tare the instrument before use.
    * - Instrumental
      - Calibration error
      - Scale or sensor is incorrectly calibrated.
      - Verify against a known standard; recalibrate or replace.
    * - Observational
      - Parallax error
      - Scale consistently viewed from an incorrect angle.
      - Read at eye level; use a mirror scale to confirm alignment.
    * - Method
      - Method limitation
      - Experimental design introduces inherent bias.
      - Identify the design flaw and redesign the method.
    * - Environmental
      - Constant temperature / lighting bias
      - Conditions consistently differ from intended controls.
      - Control or correct the environmental condition before data collection.

----

Systematic Errors Quiz
------------------------------------

.. admonition:: Fill in the Gaps — Systematic Errors
    :class: cloze

    .. cloze::
        :instructions: Complete the following by filling in the missing words.

        1. Instruments should be @@zeroed@@ before use to remove any zero error.
        2. Measuring devices must be @@calibrated@@ against a known standard to ensure accuracy.
        3. Scales should be @@read@@ at eye level to avoid parallax error.
        4. Environmental conditions should be @@controlled@@ to prevent systematic bias.
        5. If the method introduces bias, the experiment should be @@redesigned@@.

----

.. admonition:: Multiple-Choice Questions
    :class: mcq

    Choose the best answer for each question.

    .. tab-set::

        .. tab-item:: Q1

            .. multichoicepage::

                Why does repeating trials fail to reduce or eliminate a systematic error?

                [ ] Systematic errors only affect a single, isolated measurement.
                [x] The error creates a consistent bias in the same direction every time.
                [ ] Repeating trials only improves accuracy, not precision.

        .. tab-item:: Q2

            .. multichoicepage::

                An balance balance scale shows a reading of 0.25 g before any object is placed on it. What type of instrumental systematic error is this?

                [x] Zero error
                [ ] Calibration error
                [ ] Method limitation

        .. tab-item:: Q3

            .. multichoicepage::

                Which experimental aspect is primarily reduced when systematic errors are present in a set of measurements?

                [ ] Precision
                [x] Accuracy
                [ ] Sample size

        .. tab-item:: Q4

            .. multichoicepage::

                An experiment consistently yields incorrect heat transfer values because heat loss to the surrounding air was not accounted for in the setup design. What type of error source is this?

                [ ] Environmental variation
                [ ] Instrumental error
                [x] Method limitation

        .. tab-item:: Q5

            .. multichoicepage::

                What is the correct action to fix or compensate for a calibration error found in a sensor?

                [ ] Take multiple readings and calculate the average.
                [x] Verify against a known standard and recalibrate the device.
                [ ] Discard the entire data set and repeat the trial with a different operator.






