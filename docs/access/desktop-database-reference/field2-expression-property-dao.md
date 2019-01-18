---
title: Propiedad Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720089"
---
# <a name="field2expression-property-dao"></a>Propiedad Field2.Expression (DAO)

**Se aplica a**: Access 2013, Office 2013

Obtiene o establece una expresión que representa la fórmula para un campo calculado. **Cadena** de lectura y escritura.

## <a name="version-information"></a>Información de versión

Versión agregada: Access 2010

## <a name="syntax"></a>Sintaxis

*expresión* . Expresión

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Observaciones

En Access 2013, puede crear los campos de tabla que calculan valores. Los cálculos pueden incluir los valores de campos en la misma tabla, así como las funciones integradas de acceso.

El cálculo no puede incluir campos de otras tablas o consultas.

Los resultados del cálculo son de solo lectura.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

