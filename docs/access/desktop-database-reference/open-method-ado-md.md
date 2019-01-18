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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703835"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="dae29-102">Open (método, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="dae29-102">Open method (ADO MD)</span></span>

<span data-ttu-id="dae29-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dae29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dae29-104">Recupera los resultados de una consulta multidimensional y devuelve los resultados a un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="dae29-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dae29-105">Syntax</span></span>

<span data-ttu-id="dae29-106">*Conjunto de celdas*. Abrir*origen*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="dae29-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="dae29-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dae29-107">Parameters</span></span>

|<span data-ttu-id="dae29-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dae29-108">Parameter</span></span>|<span data-ttu-id="dae29-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dae29-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dae29-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="dae29-110">*Source*</span></span> |<span data-ttu-id="dae29-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dae29-111">Optional.</span></span> <span data-ttu-id="dae29-112">Un valor **Variant** que da como resultado una consulta multidimensional válida, como una consulta de expresión multidimensional (MDX).</span><span class="sxs-lookup"><span data-stu-id="dae29-112">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="dae29-113">El argumento *Source* corresponde a la propiedad [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="dae29-113">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="dae29-114">Para obtener más información acerca de MDX, vea la documentación de OLE DB para OLAP en el SDK de Microsoft Data Access Components.</span><span class="sxs-lookup"><span data-stu-id="dae29-114">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="dae29-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="dae29-115">*ActiveConnection*</span></span> |<span data-ttu-id="dae29-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dae29-116">Optional.</span></span> <span data-ttu-id="dae29-117">Un valor **Variant** que da como resultado una cadena que especifica un nombre válido de variable de objeto [Connection](connection-object-ado.md) de ADO o una definición para una conexión.</span><span class="sxs-lookup"><span data-stu-id="dae29-117">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="dae29-118">El argumento *ActiveConnection* especifica la conexión en la que se va a abrir el objeto de [conjunto de celdas](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="dae29-118">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="dae29-119">Si pasa una definición de conexión para este argumento, ADO abre una conexión nueva con los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="dae29-119">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="dae29-120">El argumento *ActiveConnection* corresponde a la propiedad [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="dae29-120">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dae29-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dae29-121">Remarks</span></span>

<span data-ttu-id="dae29-122">El método **Open** genera un error si se omite cualquiera de sus parámetros y si no se ha establecido el correspondiente valor de la propiedad antes de intentar abrir el **conjunto de celdas**.</span><span class="sxs-lookup"><span data-stu-id="dae29-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

