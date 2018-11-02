---
title: onReadyStateChange (evento, RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e52ef236a5e57efc965a6b3bd8ab6edd7533f2c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922212"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="1e279-102">onReadyStateChange (evento, RDS)</span><span class="sxs-lookup"><span data-stu-id="1e279-102">onReadyStateChange event (RDS)</span></span>


<span data-ttu-id="1e279-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e279-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1e279-104">El evento **onReadyStateChange** recibe una llamada cuando el valor de la propiedad [ReadyState](readystate-property-rds.md) cambia.</span><span class="sxs-lookup"><span data-stu-id="1e279-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e279-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e279-105">Syntax</span></span>

<span data-ttu-id="1e279-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="1e279-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="1e279-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e279-107">Parameters</span></span>

<span data-ttu-id="1e279-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1e279-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e279-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e279-109">Remarks</span></span>

<span data-ttu-id="1e279-p101">La propiedad **ReadyState** refleja el progreso de un objeto [RDS.DataControl](datacontrol-object-rds.md) a medida que recupera asincrónicamente datos en su objeto [Recordset](recordset-object-ado.md). Use el evento **onReadyStateChange** para supervisar los cambios que se produzcan en la propiedad **ReadyState**. Este método resulta más eficiente que comprobar periódicamente el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1e279-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

