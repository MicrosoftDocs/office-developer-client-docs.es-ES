---
title: Create (método, ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 866faae5d8c99258075a81f504fa9ce069f4690a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949379"
---
# <a name="create-method-adox"></a><span data-ttu-id="78719-102">Create (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="78719-102">Create method (ADOX)</span></span>

<span data-ttu-id="78719-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78719-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78719-104">Crea un nuevo catálogo.</span><span class="sxs-lookup"><span data-stu-id="78719-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="78719-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78719-105">Syntax</span></span>

<span data-ttu-id="78719-106">*Catálogo*. Crear*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="78719-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="78719-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78719-107">Parameters</span></span>

|<span data-ttu-id="78719-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="78719-108">Parameter</span></span>|<span data-ttu-id="78719-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="78719-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="78719-110">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="78719-110">*ConnectString*</span></span> |<span data-ttu-id="78719-111">Un valor **String** que se utiliza para conectarse al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="78719-111">A **String** value used to connect to the data source.</span></span>|

## <a name="remarks"></a><span data-ttu-id="78719-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78719-112">Remarks</span></span>

<span data-ttu-id="78719-p101">El método **Create** crea y abre una nueva [conexión](connection-object-ado.md) de ADO con el origen de datos especificado en *ConnectString*. Si se ejecuta correctamente, el nuevo objeto **Connection** se asigna a la propiedad [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="78719-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="78719-115">Si el proveedor no admite la creación de catálogos nuevos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="78719-115">An error will occur if the provider does not support creating new catalogs.</span></span>

