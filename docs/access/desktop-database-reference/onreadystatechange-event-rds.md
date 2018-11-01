---
title: onReadyStateChange (evento, RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869235"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="3760a-102">onReadyStateChange (evento, RDS)</span><span class="sxs-lookup"><span data-stu-id="3760a-102">onReadyStateChange Event (RDS)</span></span>


<span data-ttu-id="3760a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3760a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3760a-104">El evento **onReadyStateChange** recibe una llamada cuando el valor de la propiedad [ReadyState](readystate-property-rds.md) cambia.</span><span class="sxs-lookup"><span data-stu-id="3760a-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3760a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3760a-105">Syntax</span></span>

<span data-ttu-id="3760a-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="3760a-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="3760a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3760a-107">Parameters</span></span>

<span data-ttu-id="3760a-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3760a-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="3760a-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3760a-109">Remarks</span></span>

<span data-ttu-id="3760a-p101">La propiedad **ReadyState** refleja el progreso de un objeto [RDS.DataControl](datacontrol-object-rds.md) a medida que recupera asincrónicamente datos en su objeto [Recordset](recordset-object-ado.md). Use el evento **onReadyStateChange** para supervisar los cambios que se produzcan en la propiedad **ReadyState**. Este método resulta más eficiente que comprobar periódicamente el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3760a-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

