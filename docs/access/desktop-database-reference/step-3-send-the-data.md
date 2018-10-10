---
title: 'Paso 3: Enviar los datos'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3e6bfd6fe3b6727055eb264b1261b13d7a5a0b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483541"
---
# <a name="step-3-send-the-data"></a><span data-ttu-id="bf4b3-102">Paso 3: Enviar los datos</span><span class="sxs-lookup"><span data-stu-id="bf4b3-102">Step 3: Send the Data</span></span>


<span data-ttu-id="bf4b3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf4b3-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="bf4b3-104">Paso 3: Enviar los datos</span><span class="sxs-lookup"><span data-stu-id="bf4b3-104">Step 3: Send the Data</span></span>

<span data-ttu-id="bf4b3-p101">Ahora que ya tiene un **Recordset**, deberá enviarlo al cliente guardándolo como XML en el objeto **Response**. Agregue el código siguiente al final de XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="bf4b3-p101">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object. Add the following code to the bottom of XMLResponse.asp:</span></span>

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

<span data-ttu-id="bf4b3-107">Tenga en cuenta que el objeto de **respuesta** de ASP se especifica como el destino para el método **Recordset** [Guardar](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4b3-107">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="bf4b3-108">El destino del método **Save** puede ser cualquier objeto que admita la interfaz **IStream**, tal como un objeto ADO [Stream](stream-object-ado.md) o un nombre de archivo que incluya la ruta de acceso completa donde se va a guardar el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bf4b3-108">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

<span data-ttu-id="bf4b3-109">Antes de ir al paso siguiente, guarde y cierre XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="bf4b3-109">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="bf4b3-110">Copie también el archivo adovbs.inc desde C:\\archivos de programa\\archivos comunes\\System\\carpeta de Ado en la misma carpeta donde se encuentra el archivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="bf4b3-110">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

<span data-ttu-id="bf4b3-111">**Siguiente** [Paso 4: recibir los datos](step-4-receive-and-display-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="bf4b3-111">**Next** [Step 4: Receive the Data](step-4-receive-and-display-the-data.md)</span></span>

