---
title: Dirección URL (propiedad, RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483304"
---
# <a name="url-property-rds"></a><span data-ttu-id="b1544-102">URL (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="b1544-102">URL Property (RDS)</span></span>


<span data-ttu-id="b1544-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1544-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="b1544-104">Indica una cadena que contiene una dirección URL relativa o absoluta.</span><span class="sxs-lookup"><span data-stu-id="b1544-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="b1544-105">Puede establecer la propiedad **URL** durante el diseño en las etiquetas OBJECT del objeto [DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.</span><span class="sxs-lookup"><span data-stu-id="b1544-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1544-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1544-106">Syntax</span></span>

<span data-ttu-id="b1544-107">Tiempo de diseño: \<PARAM NAME = "URL" VALUE = "Servidor"\></span><span class="sxs-lookup"><span data-stu-id="b1544-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="b1544-108">Tiempo de ejecución: DataControl.URL="Server"</span><span class="sxs-lookup"><span data-stu-id="b1544-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="b1544-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1544-109">Parameters</span></span>

  - <span data-ttu-id="b1544-110">*Server*</span><span class="sxs-lookup"><span data-stu-id="b1544-110">*Server*</span></span>

  - <span data-ttu-id="b1544-111">Un valor de tipo **String** que contiene una dirección URL válida.</span><span class="sxs-lookup"><span data-stu-id="b1544-111">A **String** value that contains a valid URL.</span></span>

  - <span data-ttu-id="b1544-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b1544-112">*DataControl*</span></span>

  - <span data-ttu-id="b1544-113">Una variable de objeto que representa un objeto **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="b1544-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1544-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1544-114">Remarks</span></span>

<span data-ttu-id="b1544-p101">Normalmente, la dirección URL identifica a un archivo de páginas Active Server (.asp) que puede producir y devolver un objeto [Recordset](recordset-object-ado.md). Por lo tanto, el usuario puede obtener un objeto **Recordset** sin necesidad de llamar al objeto [DataFactory](datafactory-object-rdsserver.md) del servidor ni programar un objeto de negocio personalizado.</span><span class="sxs-lookup"><span data-stu-id="b1544-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="b1544-117">Si la propiedad **URL** se ha establecido, [SubmitChanges](submitchanges-method-rds.md) enviará los cambios a la ubicación especificada por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b1544-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

