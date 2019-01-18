---
title: Create (método, ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718318"
---
# <a name="create-method-adox"></a><span data-ttu-id="8c86a-102">Create (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="8c86a-102">Create method (ADOX)</span></span>

<span data-ttu-id="8c86a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c86a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c86a-104">Crea un nuevo catálogo.</span><span class="sxs-lookup"><span data-stu-id="8c86a-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c86a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c86a-105">Syntax</span></span>

<span data-ttu-id="8c86a-106">*Catálogo*. Crear*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="8c86a-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="8c86a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c86a-107">Parameters</span></span>

|<span data-ttu-id="8c86a-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8c86a-108">Parameter</span></span>|<span data-ttu-id="8c86a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c86a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8c86a-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="8c86a-110">*ConnectString*</span></span> |<span data-ttu-id="8c86a-111">Un valor **String** que se utiliza para conectarse al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8c86a-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8c86a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c86a-112">Remarks</span></span>

<span data-ttu-id="8c86a-p101">El método **Create** crea y abre una nueva [conexión](connection-object-ado.md) de ADO con el origen de datos especificado en *ConnectString*. Si se ejecuta correctamente, el nuevo objeto **Connection** se asigna a la propiedad [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8c86a-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="8c86a-115">Si el proveedor no admite la creación de catálogos nuevos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8c86a-115">An error will occur if the provider does not support creating new catalogs.</span></span>

