---
title: Propiedad Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 06/04/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 43afbfda8c560eafb90e6a53d85207e19e5b1170
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675753"
---
# <a name="recordsetfilter-property-dao"></a>Propiedad Recordset.Filter (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que determina los registros incluidos en un objeto **Recordset** abierto posteriormente (solo en áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expression*.**Filter**

*expression* Expresión que devuelve un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un tipo de datos String que contiene la cláusula WHERE de una instrucción SQL sin la palabra reservada WHERE.

Use la propiedad **Filter** para aplicar un filtro a un objeto **Recordset** de tipo Dynaset, Snapshot o solo avance.

Puede usar la propiedad **Filter** para limitar los registros que se devuelven desde un objeto existente cuando un nuevo objeto **Recordset** se abre basado en un objeto **Recordset** existente.

Utilice el formato de fecha de Estados Unidos (mes-día-año) cuando filtre campos que contengan fechas, incluso si no está utilizando una versión de Estados Unidos del motor de base de datos Microsoft Access (en cuyo caso debe reunir cualquier fecha concatenando cadenas, por ejemplo, strMonth & "-" & strDay & "-" & strYear). De lo contrario, puede que no se filtren los datos de la forma esperada.

En mucho casos, es más rápido abrir un nuevo objeto **Recordset** mediante una instrucción SQL que incluya una cláusula WHERE.

Si configura la propiedad en una cadena concatenada con un valor no entero y los parámetros del sistema especifican un carácter decimal distinto del estándar de Estados Unidos, como una coma (por ejemplo, strFilter = "PRICE \> " & lngPrice y lngPrice = 125,50), aparecerá un error cuando intente abrir el siguiente objeto **Recordset**. Esto se produce porque durante la concatenación, el número se convertirá en una cadena usando el carácter decimal predeterminado del sistema y Microsoft Access SQL solo acepta caracteres decimales con el formato estándar de Estados Unidos.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra cómo usar la propiedad Filter para determinar los registros que se incluirán en un Recordset que se abrirá posteriormente.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
