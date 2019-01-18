---
title: EjecutarSQL (acción de macro)
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704584"
---
# <a name="runsql-macro-action"></a>EjecutarSQL (acción de macro)

**Se aplica a**: Access 2013, Office 2013

La acción **EjecutarSQL** se usa para ejecutar una consulta de acción de Access mediante la correspondiente instrucción SQL. También puede ejecutar una consulta de definición de datos.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **EjecutarSQL** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Instrucción SQL</strong></p></td>
<td><p>La instrucción SQL para la consulta de acción o consulta de definición de datos que desea ejecutar. Esta instrucción puede tener como máximo 255 caracteres. Este argumento es obligatorio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Usar transacción</strong></p></td>
<td><p>Seleccione <strong>Sí</strong> para incluir esta consulta en una transacción. Seleccione <strong>No</strong> si no desea usar una transacción. El valor predeterminado es <strong>Sí</strong>. Si selecciona <strong>No</strong> para este argumento, la consulta se podría ejecutar más rápidamente.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Las consultas de acción se utilizan para anexar, eliminar y actualizar registros y para guardar el conjunto de resultados de una consulta como una nueva tabla. Las consultas de definición de datos se utilizan para crear, modificar y eliminar tablas, y para crear y eliminar índices. Puede usar la acción **EjecutarSQL** para realizar estas operaciones directamente desde una macro sin tener que usar consultas almacenadas.

Si necesita escribir una instrucción SQL que sea mayor de 255 caracteres, use en su lugar el método **RunSQL** del objeto **DoCmd** en un módulo de Visual Basic para Aplicaciones (VBA). En VBA, puede escribir instrucciones SQL de hasta 32.768 caracteres.

Las consultas de Access son en realidad instrucciones SQL que se crean cuando se diseña una consulta con la cuadrícula de diseño en la ventana Consulta. La siguiente tabla muestra las consultas de acción y las consultas de definición de datos de Access y sus correspondientes instrucciones SQL.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de consulta</p></th>
<th><p>Instrucción SQL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Acción</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Anexar</p></td>
<td><p>INSERT INTO</p></td>
</tr>
<tr class="odd">
<td><p>Eliminar</p></td>
<td><p>DELETE</p></td>
</tr>
<tr class="even">
<td><p>Creación de tabla</p></td>
<td><p>SELECCIONE... EN</p></td>
</tr>
<tr class="odd">
<td><p>Actualizar</p></td>
<td><p>UPDATE</p></td>
</tr>
<tr class="even">
<td><p><strong>Definición de datos (específico de SQL)</strong></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear una tabla</p></td>
<td><p>CREATE TABLE</p></td>
</tr>
<tr class="even">
<td><p>Modificar una tabla</p></td>
<td><p>ALTER TABLE</p></td>
</tr>
<tr class="odd">
<td><p>Eliminar una tabla</p></td>
<td><p>DROP TABLE</p></td>
</tr>
<tr class="even">
<td><p>Crear un índice</p></td>
<td><p>CREATE INDEX</p></td>
</tr>
<tr class="odd">
<td><p>Eliminar un índice</p></td>
<td><p>DROP INDEX</p></td>
</tr>
</tbody>
</table>

También puede usar una cláusula IN con estas instrucciones para modificar datos de otra base de datos.

> [!NOTE]
> [!NOTA] Para ejecutar una consulta de selección o una consulta de tabla de referencias cruzadas desde una macro, use el argumento Vista de la acción **AbrirConsulta** para abrir una consulta de selección o una consulta de tabla de referencias cruzadas existente en la vista Hoja de datos. También puede ejecutar consultas de acción y consultas específicas de SQL existentes de la misma manera.
