---
title: Propiedad Recordset.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e267e913ed89707ca79642b96dafa2cae85a574
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927538"
---
# <a name="recordsetupdateoptions-property-dao"></a>Propiedad Recordset.UpdateOptions (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . UpdateOptions

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

Cuando se ejecuta **[Update](recordset-update-method-dao.md)** en modo por lotes, DAO y la biblioteca de cursores por lotes cliente crean una serie de instrucciones SQL UPDATE para realizar los cambios necesarios. Se crea una cláusula SQL WHERE para cada actualización para aislar los registros marcados como modificados por la propiedad **[RecordStatus](recordset-recordstatus-property-dao.md)**. Como algunos servidores remotos usan desencadenadores u otras formas para aplicar la integridad referencial, con frecuencia es importante limitar la actualización de los campos solo a los afectados por el cambio. 

Para ello, establezca la propiedad **UpdateOptions** en una de las siguientes constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** o **dbCriteriaTimeStamp**. De esta forma, solo se ejecuta la cantidad mínima total de código desencadenador. Como resultado, la operación de actualización se ejecuta con más rapidez y con menos errores potenciales.

También puede concatenar cualquiera de las constantes **dbCriteriaDeleteInsert** o **dbCriteriaUpdate** para determinar si debe utilizar un conjunto de instrucciones SQL DELETE e INSERT o una instrucción SQL UPDATE para cada actualización cuando se devuelven modificaciones por lotes al servidor. En el primer caso, se requieren dos operaciones distintas para actualizar el registro. En algunos casos, sobre todo cuando el sistema remoto implementa los desencadenadores DELETE, INSERT y UPDATE, al elegir el valor correcto de la propiedad **UpdateOptions** se puede afectar significativamente en el rendimiento.

Si no especifica ninguna de las constantes, se utilizarán **dbCriteriaUpdate** y **dbCriteriaKey**.

Los registros nuevos agregados generarán siempre instrucciones INSERT y los registros eliminados generarán siempre instrucciones DELETE, por lo que esta propiedad sólo se aplica a la forma en que la biblioteca de cursores actualiza los registros modificados.

## <a name="example"></a>Ejemplo

En este ejemplo se usan las propiedades **BatchSize** y **UpdateOptions** para controlar aspectos de una actualización por lotes para el objeto **Recordset** especificado.

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

