---
title: SubmitChanges (RDS) (método)
TOCTitle: SubmitChanges Method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3227d6a8f7071ee4cdd95aa73c56d8bf61d9e26e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485005"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="db9c4-102">SubmitChanges (RDS) (método)</span><span class="sxs-lookup"><span data-stu-id="db9c4-102">SubmitChanges Method (RDS)</span></span>


<span data-ttu-id="db9c4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="db9c4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="db9c4-104">Envía los cambios pendientes del objeto [Recordset](recordset-object-ado.md) almacenado en caché local y actualizable al origen de datos especificado en la propiedad [Connect](connect-property-rds.md) o la propiedad [URL](url-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="db9c4-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db9c4-105">Syntax</span></span>

<span data-ttu-id="db9c4-106">*DataControl*. SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="db9c4-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="db9c4-107">*DataFactory*. SubmitChanges*conexión*, *conjunto de registros*</span><span class="sxs-lookup"><span data-stu-id="db9c4-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="db9c4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db9c4-108">Parameters</span></span>

  - <span data-ttu-id="db9c4-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="db9c4-109">*DataControl*</span></span>

  - <span data-ttu-id="db9c4-110">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="db9c4-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="db9c4-111">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="db9c4-111">*DataFactory*</span></span>

  - <span data-ttu-id="db9c4-112">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="db9c4-112">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="db9c4-113">*Connection*</span><span class="sxs-lookup"><span data-stu-id="db9c4-113">*Connection*</span></span>

  - <span data-ttu-id="db9c4-114">Valor de tipo **String** que representa la conexión creada con la propiedad **Connect** del objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="db9c4-114">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>

  - <span data-ttu-id="db9c4-115">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="db9c4-115">*Recordset*</span></span>

  - <span data-ttu-id="db9c4-116">Variable de objeto que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="db9c4-116">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9c4-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db9c4-117">Remarks</span></span>

<span data-ttu-id="db9c4-118">Las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) deben establecerse primero para que se pueda utilizar el método **SubmitChanges** con el objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="db9c4-118">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="db9c4-119">Si se llama al método [CancelUpdate](cancelupdate-method-rds.md) después de llamar a **SubmitChanges** del mismo objeto **Recordset**, la llamada a **CancelUpdate** generará un error porque ya se han confirmado los cambios.</span><span class="sxs-lookup"><span data-stu-id="db9c4-119">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="db9c4-120">Sólo se envían los registros cambiados para su modificación. Los cambios se realizan todos correctamente, o bien, todos juntos generan un error.</span><span class="sxs-lookup"><span data-stu-id="db9c4-120">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="db9c4-121">**SubmitChanges** puede utilizarse únicamente con el objeto **RDSServer.DataFactory** *predeterminado* .</span><span class="sxs-lookup"><span data-stu-id="db9c4-121">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="db9c4-122">Los objetos de negocio personalizados no pueden utilizar este método.</span><span class="sxs-lookup"><span data-stu-id="db9c4-122">Custom business objects can't use this method.</span></span>

<span data-ttu-id="db9c4-123">Si se ha definido la propiedad **URL**, **SubmitChanges** enviará los cambios a la ubicación especificada por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="db9c4-123">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

