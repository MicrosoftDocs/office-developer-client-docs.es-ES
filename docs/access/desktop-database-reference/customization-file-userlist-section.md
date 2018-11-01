---
title: Sección UserList del archivo de personalización
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4aa7604edc887e97cbdfbea9b75e6f46ad55f35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880771"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="ff662-102">Sección UserList del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="ff662-102">Customization File UserList Section</span></span>


<span data-ttu-id="ff662-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff662-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff662-104">La sección **userlist** pertenece a la sección **connect** con el mismo parámetro *identifier* de sección.</span><span class="sxs-lookup"><span data-stu-id="ff662-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="ff662-105">En esta sección puede contener una *entrada de acceso de usuario*, que especifica los derechos de acceso para el usuario especificado y reemplaza la *entrada de acceso* de *predeterminada* en la correspondiente sección **connect** .</span><span class="sxs-lookup"><span data-stu-id="ff662-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff662-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff662-106">Syntax</span></span>

<span data-ttu-id="ff662-107">Una entrada de acceso de usuario tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="ff662-107">A user access entry is of the form:</span></span>

<span data-ttu-id="ff662-108">*userName \*\*\* =* accessRights \*\*\*</span><span class="sxs-lookup"><span data-stu-id="ff662-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff662-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ff662-109">Part</span></span></p></th>
<th><p><span data-ttu-id="ff662-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff662-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff662-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="ff662-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="ff662-p101"><em>Nombre de usuario</em> de la persona que utiliza esta conexión. Para configurar nombres de usuario válidos, utilice el cuadro de diálogo <strong>Administrador de servicios</strong> de IIS.</span><span class="sxs-lookup"><span data-stu-id="ff662-p101">The <em>user name</em> of the person employing this connection. Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff662-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="ff662-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="ff662-115">Uno de los siguientes derechos de acceso:
</span><span class="sxs-lookup"><span data-stu-id="ff662-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="ff662-116"><strong>NoAccess</strong> el usuario no puede obtener acceso al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ff662-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="ff662-117"><strong>ReadOnly</strong> el usuario puede leer el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ff662-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="ff662-118"><strong>ReadWrite</strong> el usuario puede leer o escribir en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ff662-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

