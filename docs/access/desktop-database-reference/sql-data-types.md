---
title: Tipos de datos SQL (referencia de la base de datos de escritorio de Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308585"
---
# <a name="sql-data-types"></a>Tipos de datos SQL

**Se aplica a:** Access 2013, Office 2013

Los tipos de datos SQL del motor de base de datos de Microsoft Access están formados por 13 tipos de datos principales definidos por el motor de base de datos Microsoft Jet y varios sinónimos válidos reconocidos para estos tipos de datos.

En la tabla siguiente se enumeran los tipos de datos principales. Los sinónimos se identifican en [Palabras reservadas SQL del motor de base de datos de Microsoft Access](sql-reserved-words.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de datos</p></th>
<th><p>Tamaño de almacenamiento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BINARY</p></td>
<td><p>1 byte por carácter</p></td>
<td><p>En un campo de este tipo se puede almacenar cualquier tipo de datos. No se realiza ninguna conversión de los datos (por ejemplo, a texto). La forma de introducir los datos en un campo binario define cómo se mostrarán como resultado.</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 byte</p></td>
<td><p>Los valores y los campos Sí y No solo pueden contener uno de los dos valores.</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 byte</p></td>
<td><p>Un valor entero entre 0 y 255.</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 bytes</p></td>
<td><p>Entero con ajuste de escala entre – 922.337.203.685.477,5808 y 922.337.203.685.477,5807.</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (vea DOUBLE)</p></td>
<td><p>8 bytes</p></td>
<td><p>Un valor de fecha u hora entre los años 100 y 9999.</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 bits</p></td>
<td><p>Un número de identificación único que se usa con llamadas a procedimiento remoto.</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 bytes</p></td>
<td><p>Un valor de coma flotante de precisión sencilla entre -3,402823E38 y -1,401298E-45 para los valores negativos, y entre 1,401298E-45 y 3,402823E38 para los valores positivos y 0.</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 bytes</p></td>
<td><p>Un valor de coma flotante de precisión doble entre -1,79769313486232E308 y -4,94065645841247E-324 para los valores negativos, y entre 4,94065645841247E-324 y 1,79769313486232E308 para los valores positivos y 0.</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 bytes</p></td>
<td><p>Entero corto entre – 32.768 y 32.767. (Vea las Notas)</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 bytes</p></td>
<td><p>Entero largo entre – 2.147.483.648 y 2.147.483.647. (Vea las Notas)</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 bytes</p></td>
<td><p>Un tipo de datos numérico exacto que contiene valores desde 1028-1 hasta -1028-1. Se puede definir la precisión (1-28) y la escala (0-precisión definida). La precisión y escala predeterminadas son 18 y 0, respectivamente.</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>2 bytes por carácter (vea la nota)</p></td>
<td><p>De cero a un máximo de 2,14 gigabytes.</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>Según sea necesario</p></td>
<td><p>De cero a un máximo de 2,14 gigabytes. Se usa para objetos OLE.</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>2 bytes por carácter (vea las Notas)</p></td>
<td><p>De cero a 255 caracteres.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - El valor de inicialización y el incremento se pueden modificar mediante una [instrucción ALTER TABLE](alter-table-statement-microsoft-access-sql.md). Las filas nuevas insertadas en la tabla tendrán valores, basados en los nuevos valores de inicialización e incremento, que se generan automáticamente para la columna. Si los nuevos valores de inicialización e incremento pueden proporcionar valores que coinciden con los valores generados en función de los valores de inicialización e incremento anteriores, se generarán valores duplicados. Si la columna es una clave principal, la inserción de nuevas filas puede producir errores al generarse valores duplicados.
> - Para buscar el último valor que se usó para una columna de incremento automático, puede utilizar la siguiente instrucción: SELECT @@IDENTITY. No puede especificar el nombre de una tabla. El valor devuelto pertenece a la última tabla, que contenga una columna de incremento automático, que se actualizó.
