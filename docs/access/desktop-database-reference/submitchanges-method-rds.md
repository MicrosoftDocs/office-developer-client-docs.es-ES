---
title: SubmitChanges (método, RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b5c18aa12519e9206702eb2a152e6f0d084edc9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026347"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="e7baa-102">SubmitChanges (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="e7baa-102">SubmitChanges method (RDS)</span></span>

<span data-ttu-id="e7baa-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7baa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7baa-104">Envía los cambios pendientes del objeto [Recordset](recordset-object-ado.md) almacenado en caché local y actualizable al origen de datos especificado en la propiedad [Connect](connect-property-rds.md) o la propiedad [URL](url-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e7baa-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7baa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7baa-105">Syntax</span></span>

<span data-ttu-id="e7baa-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="e7baa-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="e7baa-107">*DataFactory*. SubmitChanges*conexión*, *conjunto de registros*</span><span class="sxs-lookup"><span data-stu-id="e7baa-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="e7baa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7baa-108">Parameters</span></span>

|<span data-ttu-id="e7baa-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e7baa-109">Parameter</span></span>|<span data-ttu-id="e7baa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7baa-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e7baa-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="e7baa-111">*DataControl*</span></span> |<span data-ttu-id="e7baa-112">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e7baa-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="e7baa-113">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="e7baa-113">*DataFactory*</span></span> |<span data-ttu-id="e7baa-114">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="e7baa-114">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="e7baa-115">*Connection*</span><span class="sxs-lookup"><span data-stu-id="e7baa-115">*Connection*</span></span> |<span data-ttu-id="e7baa-116">Valor de tipo **String** que representa la conexión creada con la propiedad **Connect** del objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e7baa-116">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>|
|<span data-ttu-id="e7baa-117">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="e7baa-117">*Recordset*</span></span> |<span data-ttu-id="e7baa-118">Variable de objeto que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e7baa-118">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e7baa-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7baa-119">Remarks</span></span>

<span data-ttu-id="e7baa-120">Las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) deben establecerse primero para que se pueda utilizar el método **SubmitChanges** con el objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e7baa-120">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="e7baa-121">Si se llama al método [CancelUpdate](cancelupdate-method-rds.md) después de llamar a **SubmitChanges** del mismo objeto **Recordset**, la llamada a **CancelUpdate** generará un error porque ya se han confirmado los cambios.</span><span class="sxs-lookup"><span data-stu-id="e7baa-121">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="e7baa-122">Sólo se envían los registros cambiados para su modificación. Los cambios se realizan todos correctamente, o bien, todos juntos generan un error.</span><span class="sxs-lookup"><span data-stu-id="e7baa-122">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="e7baa-123">**SubmitChanges** puede utilizarse únicamente con el objeto **RDSServer.DataFactory** *predeterminado* .</span><span class="sxs-lookup"><span data-stu-id="e7baa-123">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="e7baa-124">Los objetos de negocio personalizados no pueden utilizar este método.</span><span class="sxs-lookup"><span data-stu-id="e7baa-124">Custom business objects can't use this method.</span></span>

<span data-ttu-id="e7baa-125">Si se ha definido la propiedad **URL**, **SubmitChanges** enviará los cambios a la ubicación especificada por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e7baa-125">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

