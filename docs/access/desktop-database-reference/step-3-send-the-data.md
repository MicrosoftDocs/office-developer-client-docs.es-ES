---
title: 'Paso 3: Enviar los datos'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5af9b24ac7edb77ceb6dea9ceb5ae8e628fa5e3b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889710"
---
# <a name="step-3-send-the-data"></a>Paso 3: Enviar los datos


**Se aplica a**: Access 2013, Office 2013

## <a name="step-3-send-the-data"></a>Paso 3: Enviar los datos

Ahora que ya tiene un **Recordset**, deberá enviarlo al cliente guardándolo como XML en el objeto **Response**. Agregue el código siguiente al final de XMLResponse.asp:

```vb 
 
  Response.ContentType = "text/xml" 
  Response.Expires = 0 
  Response.Buffer = False 
 
 
  Response.Write "<?xml version='1.0'?>" & vbNewLine 
  adoRec.save Response, adPersistXML 
  adoRec.Close 
  Set adoRec=Nothing 
%> 
```

Tenga en cuenta que el objeto de **respuesta** de ASP se especifica como el destino para el método **Recordset** [Guardar](save-method-ado.md) . El destino del método **Save** puede ser cualquier objeto que admita la interfaz **IStream**, tal como un objeto ADO [Stream](stream-object-ado.md) o un nombre de archivo que incluya la ruta de acceso completa donde se va a guardar el objeto **Recordset**.

Antes de ir al paso siguiente, guarde y cierre XMLResponse.asp. Copie también el archivo adovbs.inc desde C:\\archivos de programa\\archivos comunes\\System\\carpeta de Ado en la misma carpeta donde se encuentra el archivo XMLResponse.asp.

### <a name="next-step"></a>Paso siguiente

[Paso 4: Recibir los datos](step-4-receive-and-display-the-data.md)

