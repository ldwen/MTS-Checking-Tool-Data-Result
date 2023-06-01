# A GUI tool to display MTS data and anomaly detection results.

![version 0.0.1](https://img.shields.io/badge/version-0.0.1-blue)
![License GNU AGPL v3](https://img.shields.io/badge/License-AGNU%20GPL%20v3-blue?logo=gnu&logoColor=white)

We have developed a dedicated graphical user interface (GUI) tool to display MTS data and assist operators in
effectively annotating data. Additionally, this tool allows visual inspection of the anomaly detection results,
including checking the abnormal data and their corresponding scores.After clone the repo, you need to

## Installation

1. Clone the repository.

2. Install the required packages.

    ```
    npm install
    npm run dev
    ```

## A Quick Guide to the GUI

1. Put the data file you want to visualize under folder ``public``

## Data Format

This tool accepts file inputs in JSON format, storing each dataset as a separate file. In cases where there are one or
more entities within a dataset, the data format for each entity is as follows:

<table>
    <tr>
        <th>Key_1</th>
        <th>Key_2</th>
        <th>Key_3/Value_1</th>
        <th>Value_2</th>
    </tr>
    <tr>
        <td rowspan="8"><i>'1'</i>(The unique index/name of the entity)</td>
        <td>'data'</td>
        <td>float value;``∈ #entities * #metrics * #time-points ``</td>
        <td></td>
    </tr>
    <tr>
        <td>'label'</td>
        <td>int value;`` ∈ #entities * #time-points`` </td>
        <td></td>
    </tr>
    <tr>
        <td rowspan="5"><i>'algorithm_a'</i>(The unique name of a algorithm)</td>
        <td> 'score' </td>
        <td>float value;`` ∈ #time-points``</td>
    </tr>
    <tr> 
        <td> 'threshold' </td>
        <td>a float value;</td>
    </tr>
    <tr> 
        <td> 'p' </td>
        <td>a float value;</td>
    </tr>
    <tr> 
        <td> 'r' </td>
        <td>a float value;</td>
    </tr>
    <tr> 
        <td> 'f1' </td>
        <td>a float value;</td>
    </tr>
    <tr>
        <td><i>'algorithm_x'</i></td>
        <td> ... </td>
        <td>...</td>
    </tr>

</table>
