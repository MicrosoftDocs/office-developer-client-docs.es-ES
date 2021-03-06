---
title: Expresiones SQL (referencia de la base de datos de escritorio de Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f38932ed4744e5479c523446f9ab77065f4eb203
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870867"
---
# <a name="sql-expressions"></a>Expresiones SQL

**Se aplica a:** Access 2013, Office 2013

Una expresión SQL es una cadena que forma total o parcialmente una instrucción SQL. Por ejemplo, el método **FindFirst** de un objeto **Recordset** usa una expresión SQL que consta de los criterios de selección incluidos en una [cláusula WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) de SQL.

El motor de base de datos de Microsoft Access usa el servicio de expresiones de Microsoft Visual Basic para Aplicaciones (VBA) para realizar sencillas evaluaciones aritméticas y de funciones. Todos los operadores usados en las expresiones SQL del motor de base de datos de Microsoft Access (excepto **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** y **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) se definen en el servicio de expresiones VBA. 

Además, el servicio de expresiones de VBA ofrece más de 100 funciones de VBA que se pueden usar en expresiones SQL. Por ejemplo, puede usar estas funciones VBA para crear una consulta SQL en la vista Diseño de consulta de Microsoft Access y también puede usarlas en una consulta SQL del método **OpenRecordset** de DAO en código de Microsoft Visual C++, Microsoft Visual Basic y Microsoft Excel.

## <a name="see-also"></a>Vea también

- [Conceptos VBA de Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
