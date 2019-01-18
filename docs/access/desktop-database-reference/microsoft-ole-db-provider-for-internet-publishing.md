---
title: OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 38183cd8306f2425a362bd2650639120a2d16845
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699782"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="76cb6-102">OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="76cb6-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="76cb6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76cb6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76cb6-p101">Microsoft OLE DB Provider for Internet Publishing permite que ADO obtenga acceso a recursos proporcionados por Microsoft FrontPage o Microsoft Internet Information Server. Los recursos incluyen archivos Web de código fuente como archivos HTML o carpetas Web de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="76cb6-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="76cb6-106">Parámetros de cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="76cb6-106">Connection string parameters</span></span>

<span data-ttu-id="76cb6-107">Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:</span><span class="sxs-lookup"><span data-stu-id="76cb6-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="76cb6-108">Este valor también puede establecerse o leerse mediante la propiedad [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="76cb6-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="76cb6-109">Cadena de conexión típica</span><span class="sxs-lookup"><span data-stu-id="76cb6-109">Typical connection string</span></span>

<span data-ttu-id="76cb6-110">Una típica cadena de conexión de este proveedor es:</span><span class="sxs-lookup"><span data-stu-id="76cb6-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="76cb6-111">\-o -</span><span class="sxs-lookup"><span data-stu-id="76cb6-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="76cb6-112">La cadena consta de estas palabras clave:</span><span class="sxs-lookup"><span data-stu-id="76cb6-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76cb6-113">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="76cb6-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="76cb6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="76cb6-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76cb6-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="76cb6-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="76cb6-116">Especifica el Proveedor OLE DB para Publicación en Internet.</span><span class="sxs-lookup"><span data-stu-id="76cb6-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76cb6-117"><strong>Data Source</strong> o <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="76cb6-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="76cb6-118">Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</span><span class="sxs-lookup"><span data-stu-id="76cb6-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76cb6-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="76cb6-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="76cb6-120">Especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="76cb6-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76cb6-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="76cb6-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="76cb6-122">Especifica la contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="76cb6-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="76cb6-p102">Si se establece el valor de *ResourceURL* desde la "URL=" de la cadena de conexión en un valor no válido, el Proveedor para Publicación en Internet muestra de forma predeterminada un cuadro de diálogo para solicitar un valor válido. Se trata de un comportamiento no deseado de un componente del nivel intermedio de una aplicación, dado que detiene la ejecución del programa hasta que se borra el cuadro de diálogo y parece que el cliente esté bloqueado debido a que no ha recibido una respuesta del componente.</span><span class="sxs-lookup"><span data-stu-id="76cb6-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="76cb6-125">Si MSDAIPP. DSO se especifica explícitamente como el valor del proveedor, ya sea con la palabra clave la cadena de conexión de *proveedor* o la propiedad **Provider** , no se puede usar "dirección URL =" en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="76cb6-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="76cb6-126">Si se hace así, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="76cb6-126">If you do, an error will occur.</span></span> <span data-ttu-id="76cb6-127">En lugar de esto, especifique la dirección URL como se muestra en el tema [Utilizar ADO con OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="76cb6-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

