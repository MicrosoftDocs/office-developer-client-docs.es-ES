---
title: Sección Logs del archivo de personalización
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28132ee681d941eda3f7c1a9b072135a2d47b12b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882836"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="69f0d-102">Sección Logs del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="69f0d-102">Customization File Logs Section</span></span>

<span data-ttu-id="69f0d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69f0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69f0d-104">La sección **Logs** contiene una entrada de archivo de registro, que especifica el nombre de un archivo que registra los errores durante el funcionamiento de **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="69f0d-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69f0d-105">Syntax</span></span>

<span data-ttu-id="69f0d-106">Una entrada de archivo de registro tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="69f0d-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69f0d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="69f0d-107">Part</span></span></p></th>
<th><p><span data-ttu-id="69f0d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="69f0d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69f0d-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="69f0d-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="69f0d-110">Cadena literal que indica que se trata de una entrada de archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="69f0d-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69f0d-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="69f0d-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="69f0d-p101">Nombre y ruta de acceso completos. El nombre de archivo suele ser <strong> c:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="69f0d-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69f0d-114">El archivo de registro contiene el nombre de usuario, HRESULT, la fecha y la hora de cada error.</span><span class="sxs-lookup"><span data-stu-id="69f0d-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

