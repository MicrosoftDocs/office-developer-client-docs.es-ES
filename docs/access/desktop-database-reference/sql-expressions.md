---
title: Expresiones SQL (referencia de escritorio de la base de datos de Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25b7d11430b730b6cedd1d8a084acd4984c5f292
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944154"
---
# <a name="sql-expressions"></a>Expresiones SQL


**Se aplica a**: Access 2013, Office 2013

Una expresión SQL es una cadena que forma total o parcialmente una instrucción SQL. Por ejemplo, el método **FindFirst** de un objeto **Recordset** usa una expresión SQL que consta de los criterios de selección incluidos en una [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) de SQL.

El motor de base de datos de Microsoft Access utiliza el servicio de expresiones de Microsoft Visual Basic para aplicaciones (o VBA) para realizar sencillas evaluaciones de aritmética y función. El servicio de expresión VBA define todos los operadores utilizados en las expresiones de SQL del motor de base de datos de Microsoft Access (excepto **[entre](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** y **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**). Además, el servicio de expresiones VBA ofrece más de 100 funciones VBA que se pueden usar en expresiones SQL. Por ejemplo, puede usar estas funciones VBA para componer una consulta SQL en la vista de diseño de la consulta de Microsoft Access, y también puede usar estas funciones en una consulta SQL en el método **OpenRecordset** DAO en Microsoft Visual C++, Microsoft Visual Basic y Microsoft Código de Excel.

