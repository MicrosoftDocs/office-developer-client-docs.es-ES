---
title: Field2.Expression Property (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92d3cd9e9ed50503b4816cae03e2a69c790706ff
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878363"
---
# <a name="field2expression-property-dao"></a>Field2.Expression Property (DAO)

**Se aplica a**: Access 2013, Office 2013

Obtiene o establece una expresión que representa la fórmula para un campo calculado. **String** de lectura y escritura.

## <a name="version-information"></a>Información de versión

Versión añadida: Access 2010


## <a name="syntax"></a>Sintaxis

*expresión* . Expresión

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Comentarios

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

