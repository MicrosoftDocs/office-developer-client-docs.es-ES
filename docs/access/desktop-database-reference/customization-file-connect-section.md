---
title: Sección Connect del archivo de personalización
TOCTitle: Customization File Connect Section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd4b7eed3cb5d8192866127322c00e7ecd5a15b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485185"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="4b676-102">Sección Connect del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="4b676-102">Customization File Connect Section</span></span>

<span data-ttu-id="4b676-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b676-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4b676-p101">El comportamiento predeterminado del controlador es denegar todas las conexiones. La sección **Connect** especifica las excepciones de ese comportamiento. Por ejemplo, si todas las secciones **Connect** están ausentes o vacías, no se podrá establecer ninguna conexión de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b676-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="4b676-107">La sección **Connect** puede contener:</span><span class="sxs-lookup"><span data-stu-id="4b676-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="4b676-p102">Una entrada de acceso predeterminada que especifica las operaciones de lectura y escritura predeterminadas que se permiten en esta conexión.Si no hay ninguna entrada de acceso predeterminada en la sección, se omitirá la sección.</span><span class="sxs-lookup"><span data-stu-id="4b676-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="4b676-110">Una nueva cadena de conexión que reemplaza la cadena de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="4b676-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b676-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b676-111">Syntax</span></span>

<span data-ttu-id="4b676-112">Una entrada de acceso predeterminada tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="4b676-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="4b676-113">Una cadena de conexión de reemplazo tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="4b676-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b676-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="4b676-114">Part</span></span></p></th>
<th><p><span data-ttu-id="4b676-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b676-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b676-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="4b676-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="4b676-117">Cadena literal que indica que se trata de una entrada de cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b676-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b676-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="4b676-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="4b676-119">Cadena que va a reemplazar toda la cadena de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="4b676-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b676-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="4b676-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="4b676-121">Cadena literal que indica que se trata de una entrada de acceso.</span><span class="sxs-lookup"><span data-stu-id="4b676-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b676-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="4b676-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="4b676-123">Uno de los siguientes derechos de acceso:
</span><span class="sxs-lookup"><span data-stu-id="4b676-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="4b676-124"><strong>NoAccess</strong> el usuario no puede obtener acceso al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="4b676-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="4b676-125"><strong>ReadOnly</strong> el usuario puede leer el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="4b676-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="4b676-126"><strong>ReadWrite</strong> el usuario puede leer o escribir en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="4b676-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b676-127">Si desea permitir cualquier conexión (en efecto, deshabilitar el comportamiento predeterminado del controlador), establezca la entrada de acceso en la sección **connect de forma predeterminada** y eliminar o cualquier otra sección de *identificador* **conectarse** en comentario.</span><span class="sxs-lookup"><span data-stu-id="4b676-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>
