---
title: 'STAT (método): ActiveX Data Objects (ADO)'
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308556"
---
# <a name="stat-method-ado"></a><span data-ttu-id="516a9-102">STAT (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="516a9-102">Stat method (ADO)</span></span>

<span data-ttu-id="516a9-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="516a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="516a9-104">Recupera información acerca de un objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="516a9-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="516a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="516a9-105">Syntax</span></span>

<span data-ttu-id="516a9-106">*Secuencia*larga. STAT (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="516a9-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="516a9-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="516a9-107">Return value</span></span>

<span data-ttu-id="516a9-108">Valor largo que indica el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="516a9-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="516a9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="516a9-109">Parameters</span></span>

|<span data-ttu-id="516a9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="516a9-110">Parameter</span></span>|<span data-ttu-id="516a9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="516a9-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="516a9-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="516a9-112">*StatStg*</span></span> |<span data-ttu-id="516a9-p101">Estructura STATSTG que se rellenará con información sobre la secuencia. La implementación del método Stat que utiliza el objeto Stream de ADO no rellena todos los campos de la estructura.</span><span class="sxs-lookup"><span data-stu-id="516a9-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="516a9-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="516a9-115">*StatFlag*</span></span> |<span data-ttu-id="516a9-p102">Especifica que este método no devuelve algunos de los miembros de la estructura STATSTG, por lo que se ahorra una operación de asignación de memoria. Los valores se toman de la enumeración STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="516a9-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="516a9-118">La enumeración STATFLAG tiene dos valores:</span><span class="sxs-lookup"><span data-stu-id="516a9-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="516a9-119">-STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="516a9-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="516a9-120">-STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="516a9-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="516a9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="516a9-121">Remarks</span></span>

<span data-ttu-id="516a9-122">La versión del método Stat implementada para el objeto Stream de ADO rellena los siguientes campos de la estructura STATSTG:</span><span class="sxs-lookup"><span data-stu-id="516a9-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="516a9-123">Field</span><span class="sxs-lookup"><span data-stu-id="516a9-123">Field</span></span>|<span data-ttu-id="516a9-124">Description</span><span class="sxs-lookup"><span data-stu-id="516a9-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="516a9-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="516a9-125">*pwcsName*</span></span> |<span data-ttu-id="516a9-126">Una cadena que contiene el nombre de la secuencia, si hay una disponible y no se ha\_especificado el valor StatFlag STATFLAG Noname.</span><span class="sxs-lookup"><span data-stu-id="516a9-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="516a9-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="516a9-127">*cbSize*</span></span> |<span data-ttu-id="516a9-128">Especifica el tamaño en bytes de la matriz de secuencias o de bytes.</span><span class="sxs-lookup"><span data-stu-id="516a9-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="516a9-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="516a9-129">*mtime*</span></span> |<span data-ttu-id="516a9-130">Indica la hora de la última modificación de esta matriz de bytes, secuencias o de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="516a9-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="516a9-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="516a9-131">*ctime*</span></span> |<span data-ttu-id="516a9-132">Indica la hora de creación de esta matriz de bytes, secuencias o de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="516a9-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="516a9-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="516a9-133">*atime*</span></span> |<span data-ttu-id="516a9-134">Indica la hora del último acceso a esta matriz de bytes, secuencias o de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="516a9-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="516a9-135">Si se\_especifica STATFLAG Noname en el parámetro STATFLAG, no se devuelve el nombre de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="516a9-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="516a9-136">Si no\_se ESPECIFICó STATFLAG Noname en el parámetro STATFLAG y no hay ningún nombre disponible para la secuencia actual, este valor será E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="516a9-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

