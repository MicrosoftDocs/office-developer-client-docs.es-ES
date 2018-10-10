---
title: Expresiones SQL (referencia de escritorio de la base de datos de Access)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 328804dc8186c082cf22d409b4071368af8873e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483348"
---
# <a name="sql-expressions"></a>Expresiones SQL


**Se aplica a**: Access 2013 | Office 2013

Una expresión SQL es una cadena que forma total o parcialmente una instrucción SQL. Por ejemplo, el método **FindFirst** de un objeto **Recordset** usa una expresión SQL que consta de los criterios de selección incluidos en una [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) de SQL.

El motor de base de datos de Microsoft Access usa el servicio de expresiones de Microsoft® Visual Basic® para Aplicaciones (VBA) para realizar sencillas evaluaciones aritméticas y de funciones. Todos los operadores usados en las expresiones SQL del motor de base de datos de Microsoft Access (excepto **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** y **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) se definen en el servicio de expresiones VBA. Además, el servicio de expresiones VBA ofrece más de 100 funciones VBA que se pueden usar en expresiones SQL. Por ejemplo, puede usar estas funciones VBA para crear una consulta SQL en la vista Diseño de consulta de Microsoft Access y también puede usarlas en una consulta SQL del método **OpenRecordset** de DAO en código de Microsoft Visual C++®, Microsoft Visual Basic y Microsoft Excel.

