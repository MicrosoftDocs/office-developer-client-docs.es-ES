---
title: Sección de registros de archivo de personalización
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295152"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="dece6-102">Sección de registros de archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="dece6-102">Customization File Logs section</span></span>

<span data-ttu-id="dece6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dece6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dece6-104">La sección **Logs** contiene una entrada de archivo de registro, que especifica el nombre de un archivo que registra los errores durante el funcionamiento de **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="dece6-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dece6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dece6-105">Syntax</span></span>

<span data-ttu-id="dece6-106">Una entrada de archivo de registro tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="dece6-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dece6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="dece6-107">Part</span></span></p></th>
<th><p><span data-ttu-id="dece6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dece6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dece6-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="dece6-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="dece6-110">Cadena literal que indica que se trata de una entrada de archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="dece6-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dece6-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="dece6-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="dece6-112">Nombre y ruta de acceso completos.</span><span class="sxs-lookup"><span data-stu-id="dece6-112">A complete path and file name.</span></span> <span data-ttu-id="dece6-113">El nombre de archivo suele ser <strong> c:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="dece6-113">The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dece6-114">El archivo de registro contiene el nombre de usuario, HRESULT, la fecha y la hora de cada error.</span><span class="sxs-lookup"><span data-stu-id="dece6-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

