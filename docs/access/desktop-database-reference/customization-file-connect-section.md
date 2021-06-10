---
title: Sección de Connect del archivo de personalización
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8652aa2c028350aab79cdf101cba189026b9a5ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295145"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="d6afa-102">Sección de Connect del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="d6afa-102">Customization File Connect section</span></span>

<span data-ttu-id="d6afa-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6afa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6afa-p101">El comportamiento predeterminado del controlador es denegar todas las conexiones. La sección **Connect** especifica las excepciones de ese comportamiento. Por ejemplo, si todas las secciones **Connect** están ausentes o vacías, no se podrá establecer ninguna conexión de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d6afa-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="d6afa-107">La sección **Connect** puede contener:</span><span class="sxs-lookup"><span data-stu-id="d6afa-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="d6afa-p102">Una entrada de acceso predeterminada que especifica las operaciones de lectura y escritura predeterminadas que se permiten en esta conexión.Si no hay ninguna entrada de acceso predeterminada en la sección, se omitirá la sección.</span><span class="sxs-lookup"><span data-stu-id="d6afa-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="d6afa-110">Una nueva cadena de conexión que reemplaza la cadena de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="d6afa-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6afa-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6afa-111">Syntax</span></span>

<span data-ttu-id="d6afa-112">Una entrada de acceso predeterminada tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="d6afa-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="d6afa-113">Una cadena de conexión de reemplazo tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="d6afa-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6afa-114">Parte</span><span class="sxs-lookup"><span data-stu-id="d6afa-114">Part</span></span></p></th>
<th><p><span data-ttu-id="d6afa-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6afa-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6afa-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="d6afa-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="d6afa-117">Cadena literal que indica que se trata de una entrada de cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="d6afa-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6afa-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="d6afa-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="d6afa-119">Cadena que va a reemplazar toda la cadena de conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="d6afa-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6afa-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="d6afa-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="d6afa-121">Cadena literal que indica que se trata de una entrada de acceso.</span><span class="sxs-lookup"><span data-stu-id="d6afa-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6afa-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="d6afa-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="d6afa-123">Uno de los siguientes derechos de acceso:</span><span class="sxs-lookup"><span data-stu-id="d6afa-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="d6afa-124"><strong>NoAccess</strong> el usuario no puede obtener acceso al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d6afa-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="d6afa-125"><strong>ReadOnly</strong> el usuario puede leer el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d6afa-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="d6afa-126"><strong>ReadWrite</strong> el usuario puede leer o escribir en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d6afa-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6afa-127">Si desea permitir cualquier conexión (en efecto, deshabilitar el comportamiento predeterminado  del controlador), establezca la entrada de  acceso de la sección predeterminada de conexión en y elimine o comente cualquier otra sección de identificador *de* conexión.</span><span class="sxs-lookup"><span data-stu-id="d6afa-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

