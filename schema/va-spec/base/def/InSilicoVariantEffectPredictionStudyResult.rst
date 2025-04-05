.. warning:: This data class is at a **draft** maturity level and may \
    change significantly in future releases. Maturity \
    levels are described in the :ref:`maturity-model`.

**Computational Definition**

A StudyResult that reports a variant effect score from a functional assay.

**Information Model**

Some InSilicoVariantEffectPredictionStudyResult attributes are inherited from :ref:`StudyResult`.

.. list-table::
   :class: clean-wrap
   :header-rows: 1
   :align: left
   :widths: auto

   *  - Field
      - Flags
      - Type
      - Limits
      - Description
   *  - id
      -
      - string
      - 0..1
      - The 'logical' identifier of the Entity in the system of record, e.g. a UUID.  This 'id' is unique within a given system, but may or may not be globally unique outside the system. It is used within a system to reference an object from another.
   *  - name
      -
      - string
      - 0..1
      - A primary name for the entity.
   *  - description
      -
      - string
      - 0..1
      - A free-text description of the Entity.
   *  - aliases
      -
                        .. raw:: html

                            <span style="background-color: #B2DFEE; color: black; padding: 2px 6px; border: 1px solid black; border-radius: 3px; font-weight: bold; display: inline-block; margin-bottom: 5px;" title="Unordered">&#8942;</span>
      - string
      - 0..m
      - Alternative name(s) for the Entity.
   *  - extensions
      -
                        .. raw:: html

                            <span style="background-color: #B2DFEE; color: black; padding: 2px 6px; border: 1px solid black; border-radius: 3px; font-weight: bold; display: inline-block; margin-bottom: 5px;" title="Unordered">&#8942;</span>
      - :ref:`Extension`
      - 0..m
      - A list of extensions to the Entity, that allow for capture of information not directly supported by elements defined in the model.
   *  - contributions
      -
                        .. raw:: html

                            <span style="background-color: #B2DFEE; color: black; padding: 2px 6px; border: 1px solid black; border-radius: 3px; font-weight: bold; display: inline-block; margin-bottom: 5px;" title="Unordered">&#8942;</span>
      - :ref:`Contribution`
      - 0..m
      - Specific actions taken by an Agent toward the creation, modification, validation, or deprecation of an Information Entity.
   *  - reportedIn
      -
                        .. raw:: html

                            <span style="background-color: #B2DFEE; color: black; padding: 2px 6px; border: 1px solid black; border-radius: 3px; font-weight: bold; display: inline-block; margin-bottom: 5px;" title="Unordered">&#8942;</span>
      - :ref:`Document` | :ref:`iriReference`
      - 0..m
      - A document in which the the Information Entity is reported.
   *  - ancillaryResults
      -
      - object
      - 0..1
      - Dictionary of any normalized or ancillary scores
   *  - qualityMeasures
      -
                        .. raw:: html

                            <span style="background-color: #D3D3D3; color: black; padding: 2px 6px; border: 1px solid black; border-radius: 3px; font-weight: bold; display: inline-block; margin-bottom: 5px;" title="Draft Maturity Level">D</span>
      - object
      - 0..1
      - An object in which implementers can define custom fields to capture metadata about the quality/provenance of the primary data items captured in standard attributes in the main body of the Study Result. e.g. a sequencing coverage metric in a Cohort Allele Frequency Study Result.
   *  - type
      -
      - string
      - 1..1
      - MUST be "InSilicoVariantEffectPredictionStudyResult".
   *  - label
      -
      - string
      - 0..1
      - A primary name for the score
   *  - focusVariant
      -
      - :ref:`iriReference` | :ref:`Allele`
      - 1..1
      - The variant for which this annotation applies to.
   *  - transcripts
      -
                        .. raw:: html

                            <span style="background-color: #B2DFEE; color: black; padding: 2px 6px; border: 1px solid black; border-radius: 3px; font-weight: bold; display: inline-block; margin-bottom: 5px;" title="Unordered">&#8942;</span>
      - :ref:`iriReference` | :ref:`SequenceReference`
      - 0..m
      - Transcripts for which this score is applicable
   *  - score
      -
      - number
      - 0..1
      - The score of the variant effect.
   *  - categoricalImpact
      -
      - string
      - 0..1
      - The qualitative term used to classify the predicted impact (e.g., damaging).
   *  - specifiedBy
      -
      - :ref:`Method` | :ref:`iriReference`
      - 0..1
      - The assay that was used to measure the variant effect with all the various properties
   *  - sourceDataSet
      -
      - :ref:`DataSet`
      - 0..1
      - The full data set that this measurement is a part of
