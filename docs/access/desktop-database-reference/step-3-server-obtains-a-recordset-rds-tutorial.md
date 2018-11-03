---
title: 'Paso 3: El servidor obtiene un objeto Recordset (Tutorial de RDS)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddd306e95ccf9ed68848b516c6d23d45286edf63
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943839"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>Paso 3: El servidor obtiene un objeto Recordset (Tutorial de RDS)

**Se aplica a**: Access 2013, Office 2013

El programa servidor usa el texto del comando y la cadena de conexión para solicitar al origen de datos las filas deseadas. Normalmente, se utiliza ADO para recuperar este objeto **Recordset**, aunque también se podrían usar otras interfaces de acceso a datos de Microsoft, tales como OLE DB.

El aspecto de un programa servidor personalizado puede ser el siguiente:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

