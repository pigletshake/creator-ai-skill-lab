# Static Output Specification

Read this reference when composing or reviewing the final map images.

## Output set

Default to one overview plus one image per day:

```text
cover (optional only when requested)
trip overview
day 1 local map
day 2 local map
...
```

Use a mobile portrait composition. For Xiaohongshu/RedNote, default to 3:4. For another named platform, adapt to its requested format. If no platform is named, use 3:4 unless the route's geography is materially clearer in another portrait ratio.

## Overview map

The overview should contain only information needed to understand the whole trip:

- concise destination and trip-length title;
- one stable color and `DAY n` label per day;
- daily activity area, numbered route silhouette, or both;
- accommodation with a distinct neutral lodging symbol when supplied;
- only major transfers between distant daily areas;
- geographic context sufficient to understand direction and scale;
- north indicator when it helps orientation;
- required data attribution and capability-mode disclosure.

Do not place segment travel times, full reservation rules, long attraction descriptions, or every nearby station on the overview. When central days are dense and an outer day is far away, keep the overview broad and move labels to daily maps instead of shrinking all text.

## Daily local map

Use an extent tight enough that consecutive stops and nearby streets are readable. Include:

- `DAY n` and a short area/theme label;
- ordered, numbered stops;
- accommodation only when it materially explains the day's departure or return;
- actual routed line in route mode, or visibly schematic connectors in other modes;
- concise segment labels only when supported, such as `步行 10 min` or `地铁4号线`;
- decision-critical entrance/exit direction, such as `午门进 · 神武门出`;
- at most one meal area and one timing highlight when they affect the flow;
- compact reservation or closure badge only when verified.

Prefer a short timeline beside or below the map when several transport labels would overlap. A dense central route may use a local inset or a separate day map; never solve collisions by making text too small.

When the user keeps a materially inefficient original order, add one compact route-warning note such as `存在折返：按原攻略绘制`. Do not repeat the full optimization discussion on the image. When the user accepts a suggested order, use the accepted order and avoid implying that it was the source post's original route.

## Alternative-day comparison

When a day contains mutually exclusive choices, replace the ordinary daily route map with a static comparison map unless separate maps are necessary for readability.

- Title the image `DAY n｜备选方案` and state the choice count, such as `三选一`.
- Use `方案A/B/C` rather than ordinary sequential stop numbers.
- Draw separate branches from the accommodation or shared origin; do not connect one option to the next.
- Keep each option's color or line style distinct while retaining the day's overall identity.
- Show the area name and at most three supported decision factors per option.
- Prefer factors that help the traveler choose: travel burden, walking/climbing intensity, seasonal relevance, reservation requirement, and whether the option fits a half or full day.
- Do not recommend one option unless the traveler profile, dates, or weather provide a defensible reason.

If an option is itself a multi-stop route, or if more than three choices cannot remain readable at phone size, create one summary comparison followed by separate option maps.

## Label priority

When space is limited, keep information in this order:

1. stop number and attraction name;
2. route order and accommodation;
3. transport mode;
4. entrance/exit or reservation warning;
5. estimated travel time;
6. meal or photo note.

Remove lower-priority labels before allowing overlap. Use short leader lines and alternate label sides for nearby markers. Do not cover markers, other labels, or the route with opaque text blocks.

## Visual consistency

- Keep each day's color identical across the overview and daily map.
- Pair color with `DAY n` and numbers so meaning does not depend on color alone.
- Subdue the basemap; emphasize routes, markers, lodging, and labels.
- Keep lodging visually distinct from numbered attractions.
- Use readable Chinese text at phone scale.
- Avoid decorative UI controls, fake buttons, and interactive affordances.

## Required disclosures by capability mode

Route mode:

```text
路线与时间为出行参考，请以实时导航及现场情况为准。
```

Position mode:

```text
景点位置按核验坐标标注，连线仅表示游览顺序，不代表实际导航路线。
```

Schematic mode:

```text
方位示意：地点关系为近似表达，请以实际地图为准。
```

## Final review

Before delivery, inspect every exported image at phone size and confirm:

- all requested days and stops are present and ordered correctly;
- no label is clipped, covered, or illegibly small;
- overview labels are not carrying daily-detail content;
- daily maps are locally zoomed rather than repeated overview crops;
- mutually exclusive alternatives are visibly branched and never appear as one route;
- hotel and stop coordinates align with the chosen basemap;
- route/time claims match the declared capability mode;
- accepted route changes match the user's choice, while retained inefficient routes carry a compact warning;
- dynamic facts are verified or omitted;
- attribution and disclosure remain visible.
