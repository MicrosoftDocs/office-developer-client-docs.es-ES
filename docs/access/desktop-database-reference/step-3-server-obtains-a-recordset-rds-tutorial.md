---
title: 'Paso 3: El servidor obtiene un objeto Recordset (Tutorial de RDS)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8509c7869613a92acf0d61e4fb1ebc5be411c0a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485472"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>Paso 3: El servidor obtiene un objeto Recordset (Tutorial de RDS)


**Se aplica a**: Access 2013 | Office 2013

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

