---
title: Refresh (método, RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49b91f129a0661c5c81243bb405de9088b1e06d
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950121"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="97b18-102">Refresh (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="97b18-102">Refresh method (RDS)</span></span>

<span data-ttu-id="97b18-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97b18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97b18-104">Vuelve a consultar el origen de datos especificado en la propiedad [Connect](connect-property-rds.md) y actualiza los resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="97b18-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b18-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97b18-105">Syntax</span></span>

<span data-ttu-id="97b18-106">*DataControl*. Actualización</span><span class="sxs-lookup"><span data-stu-id="97b18-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="97b18-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97b18-107">Parameters</span></span>

|<span data-ttu-id="97b18-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="97b18-108">Parameter</span></span>|<span data-ttu-id="97b18-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="97b18-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="97b18-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="97b18-110">*DataControl*</span></span> |<span data-ttu-id="97b18-111">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="97b18-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="97b18-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97b18-112">Remarks</span></span>

<span data-ttu-id="97b18-p101">Debe establecer las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) antes de utilizar el método **Refresh**. Todos los controles enlazados a datos del formulario asociado a un objeto **RDS.DataControl** reflejarán el conjunto de registros nuevo. Se liberan todos los objetos [Recordset](recordset-object-ado.md) previamente existentes y se descartan todos los cambios no guardados. El método **Refresh** convierte automáticamente el primer registro en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="97b18-p101">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties before you use the **Refresh** method. All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records. Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded. The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="97b18-p102">Se recomienda llamar periódicamente al método **Refresh** cuando trabaja con datos. Si recupera datos y los deja durante un tiempo en el equipo de cliente, es probable que se vuelvan obsoletos. Es posible que se genere un error al realizar cambios porque otro usuario puede haber cambiado anteriormente el registro y enviado cambios.</span><span class="sxs-lookup"><span data-stu-id="97b18-p102">It's a good idea to call the **Refresh** method periodically when you work with data. If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date. It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

