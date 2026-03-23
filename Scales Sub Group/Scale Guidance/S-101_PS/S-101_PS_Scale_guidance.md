**1.3 Terms, definitions and abbreviations**

**1.3.1 Terms and definitions**

**maximum display scale**

The maximum scale with which the data is displayed

**minimum display scale**

The minimum scale with which the data is displayed

**viewing scale**

the value of the ratio of the linear dimensions of **features** of a **dataset** presented in the display and the actual dimensions of the **features** represented of the **dataset**

**4.5 Dataset**

**4.5.1 Introduction**

A dataset is a grouping of features, attributes, geometry and metadata
which comprises a specific coverage.

**4.5.2 Dataset rules**

In order to facilitate the efficient processing of ENC data the
geographic coverage of a given **maximum display scale** may be split
into multiple datasets.

The discovery metadata of a dataset must list all the **Data Coverage**
features contained within that dataset and their assigned scale
attributions.

An ENC update dataset must not change the limit of a **Data Coverage**
feature for the base ENC dataset. Where the limit of a **Data Coverage**
feature for a base ENC dataset is to be changed, this must be done by
issuing a new edition of the dataset.

Datasets must not cross the 180° meridian; this includes both the **Data
Coverage** features and the bounding box for the dataset.

**4.5.3 Data Coverage rules**

-   All base datasets (new dataset, new edition and re-issue) must
    contain at least one **Data Coverage** feature.

-   The data boundary of the base dataset is defined by the extent of
    the **Data Coverage** features and must be contained within the
    bounding box.

-   The **Data Coverage** features within a dataset must not overlap,
    however **Data Coverage** features from different datasets may
    overlap if they have differing maximum display scales.

-   Datasets may overlap, however there must be no overlapping **Data
    Coverage** features of the same **maximum display scale**, except at
    the agreed adjoining national data limits, where, if it is difficult
    to achieve a perfect join, a 5 metre overlapping buffer zone may be
    used; and for this situation, there must be no gaps in data.

-   When a dataset has multiple **Data Coverage** features, then the
    **minimum display scale** must be the same for all **Data Coverage**
    features within the dataset. The **maximum display scale** for
    multiple **Data Coverage** features within a dataset may be
    different.

-   When a dataset has multiple **Data Coverage** features then the
    **maximum display scale** of the dataset must be equal to the
    largest **maximum display scale** of the **Data Coverage** features.

-   The **maximum display scale** is considered to be the equivalent of
    the compilation scale of the data.

![](vertopal_48dbacc662574efc805cb17e67aadfd2/media/image1.wmf){width="5.768055555555556in"
height="3.86875in"}

**4.5.4 Dataset size**

Datasets must not exceed 10MB.

Update datasets should not normally be larger than 50kb and must not be
larger than 200kb.

**4.6 Display Scale Range**

A scale range of a dataset is used to indicate a range of scales between
which a producer considers the data is intended for use. (See clause 4.7
for how datasets are to be loaded and unloaded within a navigation
system.) The smallest scale is defined by the **minimum display scale**
and the largest scale by the **maximum display scale**. These scales
must be set at one of the scales specified in clause 3 (spatial
resolutions).

When the systems viewing scale is smaller than the value indicated by
**minimum display scale**, features within the **Data Coverage** feature
are not displayed, except where the SENC does not contain a dataset
covering the area at a smaller scale, in which case the dataset will be
displayed at all smaller scales. When the viewing scale is larger than
the value indicated by **maximum display scale**, the overscale
indication, in the form of an overscale factor and pattern covering the
area that is overscale, must be shown. When own ship's position is
covered by a dataset with a larger **maximum display scale** than the
mariner's selected viewing scale (MSVS) an indication is required and
should be shown on the same screen as the chart display.
