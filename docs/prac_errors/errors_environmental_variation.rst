==========================
Environmental Variation
==========================

| **Environmental variation** occurs when uncontrolled conditions in the experimental setting fluctuate unpredictably between trials, introducing random changes into measurements.
| It is classified as a **random error** — the direction and size of the fluctuation differs between readings, causing results to scatter around the true value.

.. note::

   If an environmental condition is *consistently* different from the
   intended condition across all trials, it produces **environmental bias**
   — a systematic error treated separately.

Examples
------------

These conditions fluctuate unpredictably between trials, causing results
to scatter around the true value:

* Air currents near a top-pan balance causing the display to fluctuate
  between readings
* Electrical noise from nearby equipment introducing fluctuations into
  the readings of a sensitive voltage or current sensor
* Vibrations from foot traffic or nearby machinery causing instability
  in balance readings between trials
* Variation in ambient light levels affecting the readings of a
  light-dependent resistor or colorimeter between trials
* Humidity fluctuating between readings, causing the mass of a
  hygroscopic substance to vary slightly between trials



.. admonition:: Environmental Variation: A Four-Step Analysis
    :class: premise

    Use the four-step framework to analyse environmental variation:

    **Step 1 — Identify the source**
        *Environment* — uncontrolled conditions in the experimental
        setting fluctuate unpredictably between trials, independent of
        the instrument, the operator, or the method design. Name the
        specific variable rather than writing "environmental error" —
        for example, "air currents near the balance" or "electrical
        noise from nearby equipment."

    **Step 2 — Classify the behaviour**
        Unpredictable spread → **Random error** → affects precision.
        The direction and magnitude of the fluctuation differs between
        trials, so results scatter around the true value rather than
        being consistently displaced in one direction.

    **Step 3 — Explain the impact**
        Results are scattered above and below the true value. No single
        trial is consistently too high or too low — the variation averages
        out over many measurements. Accuracy is not affected, but
        precision is reduced.

    **Step 4 — Suggest an improvement**
        Environmental variation is reduced, not eliminated — control or
        shield the apparatus from the source of fluctuation, and repeat
        measurements to average out the random spread.

----

Effects
----------------

Environmental variation produces **random scatter** around the true
value. Because environmental fluctuations vary unpredictably between
trials:

* results are scattered above and below the true value rather than
  consistently displaced in one direction,
* **precision is reduced** — repeated readings may not agree closely
  with each other,
* **accuracy is not affected** — there is no consistent bias; results
  are centred on the true value on average,
* repeating measurements and averaging will reduce the effect, since
  random fluctuations tend to cancel out over many trials.

----

Improvements
------------

To reduce environmental variation, shield the apparatus from the source
of fluctuation and increase the number of trials.

* Shield sensitive instruments from air currents using a draught
  enclosure or by closing windows and vents near the apparatus.
* Use a Faraday cage or shielded cables to reduce electromagnetic
  interference affecting sensitive electrical measurements.
* Place the apparatus on a stable, isolated bench away from sources
  of vibration such as foot traffic or machinery.
* Complete all trials in a single session to minimise changes in
  environmental conditions between measurements.
* Repeat measurements and calculate a mean — random fluctuations tend
  to cancel out as the number of trials increases.
* Record environmental conditions (temperature, humidity, light level)
  alongside data so the source of variation can be identified and
  discussed in the evaluation.


----

.. cloze::
    :instructions: Complete the following by filling in the missing words.

    1. Environmental variation occurs when uncontrolled conditions in the experimental setting @@fluctuate@@ unpredictably between trials.
    2. Because environmental fluctuations vary unpredictably, environmental variation is classified as a @@random@@ error.
    3. According to the four-step analysis framework, environmental variation belongs to the @@Environment@@ source category.
    4. Environmental variation reduces the @@precision@@ of measurements, while accuracy remains unaffected.
    5. Environmental variation can be reduced by @@shielding@@ or controlling the apparatus and repeating measurements to calculate a mean.


.. mcqgroup::
    :show_instant_feedback:

    .. multichoice::

        Air currents near an electronic balance cause the displayed mass to fluctuate unpredictably during an experiment. How is this type of error classified?

        [ ] Systematic error
        [x] Random error
        [ ] Personal error
        [ ] Instrumental offset

    .. multichoice::

        Which of the following describes the impact of environmental variation on experimental data?

        [ ] It shifts all readings in one direction, reducing accuracy.
        [x] It causes results to scatter above and below the true value, reducing precision.
        [ ] It causes a permanent offset that cannot be reduced by averaging.
        [ ] It changes the sensitivity and calibration of the instrument.

    .. multichoice::

        How does environmental variation differ from environmental bias?

        [ ] Environmental variation affects accuracy, while environmental bias affects precision.
        [x] Environmental variation fluctuates unpredictably, whereas environmental bias is consistently shifted across all trials.
        [ ] Environmental variation is a systematic error, while environmental bias is a random error.
        [ ] Environmental variation can be completely eliminated, while environmental bias cannot.

    .. multichoice::

        Which source category from the four-step error framework does electrical noise affecting a sensor belong to?

        [ ] Instrumental
        [ ] Observation / procedure
        [ ] Method
        [x] Environment

    .. multichoice::

        Which improvement strategy is specifically aimed at reducing environmental variation in balance readings?

        [ ] Using a correction factor calculated from a known standard.
        [x] Enclosing the balance in a draught shield and using a stable bench away from foot traffic.
        [ ] Re-zeroing the balance only once at the beginning of the day.
        [ ] Changing to an analogue balance with larger scale divisions.

----

.. admonition:: Structured Question: Environmental Variation
    :class: shortanswer

    A Year 8 class is investigating whether the length of a rubber band
    affects how far it can launch a small paper ball. Each group stretches
    rubber bands of four different lengths — 5 cm, 10 cm, 15 cm, and 20 cm
    — and measures the distance the paper ball travels after launch. The
    experiment is conducted near an open window on a windy day. The students
    notice that the wind gusts are unpredictable — sometimes blowing toward
    the target, sometimes away, and sometimes not at all.

    **(a)** Identify the type of error introduced by conducting the
    experiment near the open window and classify it as random, systematic,
    or personal. *(2 marks)*

    **(b)** Explain how this error would affect the group's results. In
    your answer, refer to the direction of the error and its effect on the
    accuracy and precision of the results. *(3 marks)*

    **(c)** The group repeats each trial five times and calculates a mean
    launch distance. Evaluate whether this would reduce the effect of the
    error identified in part (a). *(2 marks)*

    **(d)** Describe one improvement the group could make to reduce this
    error before collecting data. *(1 mark)*

    .. dropdown:: Reveal Answer Key
        :icon: check-circle
        :class-container: dropdown-shortanswer

        .. tab-set::

            .. tab-item:: Model Answer

                **(a)**

                The error is **environmental variation**, classified as a
                **random error**.

                *(1 mark for naming environmental variation; 1 mark for random)*

                **(b)**

                Because the wind gusts are unpredictable in direction and
                strength, they affect each launch differently — sometimes adding
                to the distance, sometimes reducing it, and sometimes having no
                effect. There is no consistent direction to the error; results
                are scattered both above and below the true launch distance for
                each rubber band length. *(1 mark)*

                The **precision** of the results is reduced — repeated trials
                for the same rubber band length will give noticeably different
                distances because each launch is affected by a different gust.
                *(1 mark)*

                The **accuracy** is not systematically affected — because the
                wind acts in different directions across trials, the errors
                tend to cancel out over many measurements, and the mean is
                likely to be close to the true value. *(1 mark)*

                **(c)**

                Repeating each trial five times and averaging **would** help
                reduce the effect of this error, although it cannot eliminate
                it entirely. *(1 mark)*

                Because the wind gusts vary unpredictably in direction and
                strength, some trials will give distances that are too high and
                others too low. Averaging across multiple trials allows these
                opposing errors to partially cancel out, bringing the mean
                closer to the true launch distance. Increasing the number of
                trials further would improve this effect. *(1 mark)*

                **(d)**

                The group should close the window before collecting data to
                remove the source of air movement, or move to an indoor location
                away from drafts, so that wind no longer affects the launch
                distance. *(1 mark)*

            .. tab-item:: Marking Guidance

                **Part (a):** accept "environmental variation" or "random
                environmental fluctuation." Do not accept "environmental bias"
                — the wind is unpredictable in direction and strength, so there
                is no consistent offset in one direction. Do not accept
                "operator error" or "method limitation" — the wind is an
                uncontrolled external condition, not a mistake or design flaw.

                **Part (b):** award the direction mark for a response that
                correctly identifies there is no consistent direction — results
                are scattered both above and below the true value. Do not award
                this mark for a response that identifies only one direction of
                effect. Award the precision mark for correctly stating precision
                is reduced and linking this to the unpredictable variation
                between trials. Award the accuracy mark for correctly stating
                accuracy is not systematically affected because errors tend to
                cancel out across trials.

                **Part (c):** this question deliberately differs from the
                previous structured questions — repeating and averaging
                **does** help for random errors. Award both marks only if the
                student correctly identifies that averaging helps and explains
                why: opposing errors partially cancel out. A response that
                states repeating always reduces error without this reasoning
                should receive only 1 mark.

                **Part (d):** accept "shield the apparatus with a barrier to
                block air movement" or "conduct the experiment in a corridor
                away from windows" as alternative valid responses. Do not
                accept "repeat measurements" as this has already been
                addressed in part (c) and only reduces rather than eliminates
                the error.









