---
title: Open (método, ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288402"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="dffdb-102">Open (método, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="dffdb-102">Open method (ADO MD)</span></span>

<span data-ttu-id="dffdb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dffdb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dffdb-104">Recupera los resultados de una consulta multidimensional y devuelve los resultados a un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="dffdb-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffdb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dffdb-105">Syntax</span></span>

<span data-ttu-id="dffdb-106">*Conjunto de celdas*. Open *Source*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="dffdb-106">*Cellset*.Open *Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="dffdb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dffdb-107">Parameters</span></span>

|<span data-ttu-id="dffdb-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dffdb-108">Parameter</span></span>|<span data-ttu-id="dffdb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dffdb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dffdb-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="dffdb-110">*Source*</span></span> |<span data-ttu-id="dffdb-p101">Opcional. Un valor **Variant** que da como resultado una consulta multidimensional válida, como una consulta de expresión multidimensional (MDX). El argumento *Source* corresponde a la propiedad [Source](source-property-ado-md.md). Para obtener más información acerca de MDX, vea la documentación de OLE DB para OLAP en el SDK de Microsoft Data Access Components.</span><span class="sxs-lookup"><span data-stu-id="dffdb-p101">Optional. A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query. The *Source* argument corresponds to the [Source](source-property-ado-md.md) property. For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="dffdb-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="dffdb-115">*ActiveConnection*</span></span> |<span data-ttu-id="dffdb-p102">Opcional. Un valor **Variant** que da como resultado una cadena que especifica un nombre válido de variable de objeto [Connection](connection-object-ado.md) de ADO o una definición para una conexión. El argumento *ActiveConnection* especifica la conexión durante la que se abrirá el objeto [Cellset](cellset-object-ado-md.md). Si pasa una definición de conexión para este argumento, ADO abre una conexión nueva que utiliza los parámetros especificados. El argumento *ActiveConnection* corresponde a la propiedad [ActiveConnection](activeconnection-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="dffdb-p102">Optional. A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection. The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object. If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters. The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dffdb-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dffdb-121">Remarks</span></span>

<span data-ttu-id="dffdb-122">El método **Open** genera un error si se omite cualquiera de sus parámetros y si no se ha establecido el correspondiente valor de la propiedad antes de intentar abrir el **conjunto de celdas**.</span><span class="sxs-lookup"><span data-stu-id="dffdb-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

