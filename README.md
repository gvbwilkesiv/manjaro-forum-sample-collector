# Manjaro Forum Sample Collector

A student-facing, two-stage data acquisition tool for research using
topics from the Manjaro Linux forum.

## Purpose

The collector supports a research procedure in which students acquire
forum data and then perform the analytical work themselves. The
application does **not** sort, code, classify, rank, interpret, or
recommend.

## Research procedure

### Stage 1 --- Draw General Sample

The collector retrieves 100 eligible topics from **Manjaro Support →
Third-Party Software**. Pinned administrative topics are excluded.

Students download the resulting CSV, examine and code the sample, and
identify a named software or device entity that the evidence indicates
warrants closer investigation.

### Stage 2 --- Draw Named-Entity Sample

After identifying the entity, the student determines its corresponding
Manjaro tag and enters that tag in the collector.

The collector retrieves up to 100 topics carrying that tag from across
the Manjaro forum. If fewer than 100 eligible topics are available, it
returns all available topics.

## Data and provenance

Both samples preserve fields useful for subsequent analysis, including
topic title, replies, views, activity date, tags, topic ID, original
topic URL, collection timestamp, and source.

Topic titles in the web interface link to the original Manjaro
discussions.

## Analytical responsibility

The application performs **acquisition only**. Students remain
responsible for sorting, coding, classification, analysis,
interpretation, and recommendations.

## Technical note

The public interface is a static web page. Data acquisition is handled
by a restricted Cloudflare Worker that requests structured topic data
from the Manjaro forum.
