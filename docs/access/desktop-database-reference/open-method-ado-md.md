---
title: Open (método, ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad4d1c05637f2ff7ef5ff65ec26ab1b721495067
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483328"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="926dd-102">Open (método, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="926dd-102">Open Method (ADO MD)</span></span>


<span data-ttu-id="926dd-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="926dd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="926dd-104">Recupera los resultados de una consulta multidimensional y devuelve los resultados a un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="926dd-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="926dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="926dd-105">Syntax</span></span>

<span data-ttu-id="926dd-106">*Conjunto de celdas*. Abrir*origen*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="926dd-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="926dd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="926dd-107">Parameters</span></span>

  - <span data-ttu-id="926dd-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="926dd-108">*Source*</span></span>

  - <span data-ttu-id="926dd-109">Opcional.</span><span class="sxs-lookup"><span data-stu-id="926dd-109">Optional.</span></span> <span data-ttu-id="926dd-110">Un valor **Variant** que da como resultado una consulta multidimensional válida, como una consulta de expresión multidimensional (MDX).</span><span class="sxs-lookup"><span data-stu-id="926dd-110">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="926dd-111">El argumento *Source* corresponde a la propiedad [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="926dd-111">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="926dd-112">Para obtener más información acerca de MDX, vea la documentación de OLE DB para OLAP en el SDK de Microsoft Data Access Components.</span><span class="sxs-lookup"><span data-stu-id="926dd-112">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>

  - <span data-ttu-id="926dd-113">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="926dd-113">*ActiveConnection*</span></span>

  - <span data-ttu-id="926dd-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="926dd-114">Optional.</span></span> <span data-ttu-id="926dd-115">Un valor **Variant** que da como resultado una cadena que especifica un nombre válido de variable de objeto [Connection](connection-object-ado.md) de ADO o una definición para una conexión.</span><span class="sxs-lookup"><span data-stu-id="926dd-115">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="926dd-116">El argumento *ActiveConnection* especifica la conexión en la que se va a abrir el objeto de [conjunto de celdas](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="926dd-116">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="926dd-117">Si pasa una definición de conexión para este argumento, ADO abre una conexión nueva con los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="926dd-117">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="926dd-118">El argumento *ActiveConnection* corresponde a la propiedad [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="926dd-118">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="926dd-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="926dd-119">Remarks</span></span>

<span data-ttu-id="926dd-120">El método **Open** genera un error si se omite cualquiera de sus parámetros y si no se ha establecido el correspondiente valor de la propiedad antes de intentar abrir el **conjunto de celdas**.</span><span class="sxs-lookup"><span data-stu-id="926dd-120">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

