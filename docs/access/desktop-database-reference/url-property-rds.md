---
title: Propiedad URL (referencia de base de datos de escritorio de Access de RDS)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313401"
---
# <a name="url-property-rds"></a><span data-ttu-id="90c6d-102">URL (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="90c6d-102">URL property (RDS)</span></span>

<span data-ttu-id="90c6d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90c6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90c6d-104">Indica una cadena que contiene una dirección URL relativa o absoluta.</span><span class="sxs-lookup"><span data-stu-id="90c6d-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="90c6d-105">Puede establecer la propiedad **URL** durante el diseño en las etiquetas OBJECT del objeto [DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.</span><span class="sxs-lookup"><span data-stu-id="90c6d-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c6d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90c6d-106">Syntax</span></span>

<span data-ttu-id="90c6d-107">Tiempo de diseño \<: param name = "URL" Value = "Server"\></span><span class="sxs-lookup"><span data-stu-id="90c6d-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="90c6d-108">Tiempo de ejecución: DataControl. URL = "Server"</span><span class="sxs-lookup"><span data-stu-id="90c6d-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="90c6d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90c6d-109">Parameters</span></span>

|<span data-ttu-id="90c6d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90c6d-110">Parameter</span></span>|<span data-ttu-id="90c6d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="90c6d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="90c6d-112">*Server*</span><span class="sxs-lookup"><span data-stu-id="90c6d-112">*Server*</span></span> |<span data-ttu-id="90c6d-113">Un valor de tipo **String** que contiene una dirección URL válida.</span><span class="sxs-lookup"><span data-stu-id="90c6d-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="90c6d-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="90c6d-114">*DataControl*</span></span> |<span data-ttu-id="90c6d-115">Una variable de objeto que representa un objeto **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="90c6d-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="90c6d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90c6d-116">Remarks</span></span>

<span data-ttu-id="90c6d-p101">Normalmente, la dirección URL identifica a un archivo de páginas Active Server (.asp) que puede producir y devolver un objeto [Recordset](recordset-object-ado.md). Por lo tanto, el usuario puede obtener un objeto **Recordset** sin necesidad de llamar al objeto [DataFactory](datafactory-object-rdsserver.md) del servidor ni programar un objeto de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="90c6d-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="90c6d-119">Si la propiedad **URL** se ha establecido, [SubmitChanges](submitchanges-method-rds.md) enviará los cambios a la ubicación especificada por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="90c6d-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

