TASK 1: Implementing Interaction

    For this assignment, I selected the “Headway Imbalance and Bunching Diagnostic” visualization from Assignment 2. The visualization uses a scatterplot to examine the relationship between the time gap before a bus arrives and the time gap until the following bus arrives at the same stop. The horizontal axis represents the previous bus gap, measured in minutes, while the vertical axis represents the actual next bus gap, also measured in minutes. Each point represents an observed bus headway at a particular CTA stop. The points are colored according to their bus route, and their fill distinguishes between travel directions: filled circles represent northbound and westbound observations, while hollow circles represent southbound and eastbound observations. A dashed diagonal reference line, where the previous and following gaps are equal (y=x), provides a baseline for interpreting headway consistency. Points close to this line indicate that the two consecutive gaps are relatively similar. Points substantially above or below the line indicate a larger difference between the preceding and following bus intervals. For example, a point with a relatively short previous gap and a much longer following gap may indicate that buses arrived close together and were subsequently followed by a longer service gap, which can be associated with bus bunching. Both the static and interactive implementations use the same underlying CTA bus headway dataset and retain the same central visual encoding. This allows the two versions to communicate the same information while differing in how users explore and examine the observations.
    The static implementation preserves the original design from Assignment 2. It presents the observations in a single scatterplot, displaying the available routes, stops, and directions simultaneously. The static visualization uses the following visual encodings:
    - Position: The previous bus gap is encoded on the x-axis, and the actual following bus gap is encoded on the y-axis.
    - Color: Different routes are represented using distinct colors.
    - Fill: Filled circles represent northbound and westbound observations, while hollow circles represent southbound and eastbound observations.
    - Reference line: A dashed diagonal line represents equal consecutive headways.
    - Legend: The legend identifies the route, stop, and direction associated with the observations.
    Both axes use a consistent range of 0–60 minutes, with grid lines and tick marks at five-minute intervals. This makes it easier to compare observations and estimate the magnitude of differences between consecutive bus gaps. The static visualization is intended to provide an overview of the entire dataset. Users can examine the overall distribution of observations, identify potential bunching patterns, and compare routes and directions by referring to the color and symbol encodings. The legend provides the information needed to distinguish the different route and stop combinations without requiring interaction. Importantly, the static version is not intended to be a simplified or deliberately less informative version of the interactive visualization. It displays the observations together, allowing users to examine the full dataset and make comparisons across routes and stops without needing to change any settings.
    The interactive implementation retains the same scatterplot design, dataset, axes, reference line, and visual encodings. However, it introduces interactions that allow users to explore subsets of the data and examine individual observations in greater detail.

    I implemented the interactive visualization using Vega-Lite, with the following interactions:

    Route filtering

    A dropdown menu allows users to select an individual bus route or display all routes. This makes it possible to isolate a particular route and examine its headway patterns without the visual complexity of displaying every route simultaneously.

    For example, a user can select Route 36 to examine its observations independently, then switch to Route 146 to compare the distribution of headway gaps between the two routes.

    Direction filtering

    A second dropdown menu allows users to filter observations by direction: northbound, southbound, eastbound, or westbound. Users can also select all directions.

    This interaction is useful because headway patterns may differ between directions, even when observations belong to the same route. Filtering by direction makes it easier to examine whether potential bunching or irregular service intervals are concentrated in a particular direction.

    Hover tooltips

    Hovering over an individual point reveals additional information about that observation, including its observation ID, route, direction, stop name, CTA stop ID, previous bus gap, actual following bus gap, and associated comments.

    This supports details-on-demand by allowing users to inspect individual observations without displaying all of their descriptive information directly on the chart. The tooltip is particularly useful when several points are close together or when users want to understand the context behind an unusual headway pattern.

    Zooming and panning

    Users can scroll to zoom into a particular region of the scatterplot and drag to pan across the visualization. Double-clicking resets the view.

    This interaction allows users to examine clusters of observations more closely, particularly when multiple points are concentrated in a small region of the chart.

    The interactions were selected to support analytical exploration rather than simply adding visual effects. In particular, they address the difficulty of examining individual routes, directions, and observations when the entire dataset is displayed simultaneously.

    The route and direction filters support comparisons that would otherwise require users to locate and mentally separate relevant observations from the full scatterplot. Rather than relying entirely on the legend and visual search, users can isolate a subset of the data and focus on its distribution.

    The tooltip provides additional contextual information that is not immediately visible from the position and color of a point. This is useful when users identify an unusual observation and want to investigate its corresponding stop, route, or recorded comments.

    Zooming and panning provide additional support when examining dense regions of the chart. Users can focus on particular clusters and more easily distinguish individual observations.

    Together, these interactions are expected to help users complete analytical tasks involving:
    1. Identifying potential bus bunching: Recognizing observations where a relatively short previous gap is followed by a substantially longer gap.
    2. Examining headway consistency: Comparing the previous and following bus intervals relative to the equal-headway reference line.
    3. Comparing routes: Investigating whether different routes exhibit different distributions of consecutive bus gaps.
    4. Comparing directions: Determining whether headway irregularities appear more frequently in particular travel directions.
    5. Investigating individual observations: Using tooltips to identify the stop and contextual information associated with unusual points.
    5. Maintaining a meaningful comparison between the two versions
    An important consideration in the implementation was ensuring that the static visualization remained a meaningful alternative to the interactive visualization.

    Both versions use the same underlying dataset, scatterplot structure, axis definitions, route colors, directional fill encoding, and equal-headway reference line. The static version provides an overview of all observations, while the interactive version provides additional mechanisms for filtering and inspecting the same information.

    The distinction is therefore not that one version contains more underlying data than the other. Instead, the difference lies in how users access and explore that data. In the static version, users rely on the overall distribution, visual encodings, and legend to identify patterns. In the interactive version, users can actively isolate routes and directions, inspect individual observations, and explore dense regions of the chart.

    This design allows the evaluation to investigate whether interactive exploration improves the efficiency and accuracy of completing analytical tasks, rather than simply comparing a detailed visualization against an intentionally restricted static one.

    Both visualizations were implemented using Vega-Lite specifications and embedded in the evaluation interface. The interface presents participants with analytical tasks and records their answers, explanations, confidence ratings, perceived task difficulty, and time taken to complete each task.

    The evaluation includes both static and interactive conditions. The order of the conditions is counterbalanced across two participant groups to reduce the possibility that differences in performance are caused solely by participants encountering one visualization first.

    The same analytical tasks are used across the two conditions, with different routes assigned to the corresponding tasks. This provides a basis for comparing how participants interpret the headway data under each visualization condition.

    The evaluation can therefore consider several measures:
    - Task completion time: Whether participants complete analytical tasks more quickly using the interactive visualization.
    - Answer accuracy: Whether filtering and additional inspection capabilities help participants identify headway patterns correctly.
    - Confidence: Whether participants feel more confident in their interpretations when using the interactive visualization.
    - Perceived difficulty: Whether participants find particular analytical tasks easier or more difficult under either condition.
    - Written explanations: Whether participants refer to relevant visual evidence when explaining their answers.
    Overall, the expected benefit of the interactive implementation is that it reduces the effort required to isolate and investigate relevant subsets of the data. However, the static visualization may still be advantageous for tasks that benefit from seeing the entire dataset at once. The evaluation is intended to examine these differences rather than assume that the interactive version will necessarily perform better.

TASK 2: Evaluation Design

