---
title: Create (método, ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91f5105611df85e007dea6d0e17e3104ea5987a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870257"
---
# <a name="create-method-adox"></a><span data-ttu-id="82245-102">Create (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="82245-102">Create Method (ADOX)</span></span>


<span data-ttu-id="82245-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82245-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="82245-104">Crea un nuevo catálogo.</span><span class="sxs-lookup"><span data-stu-id="82245-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="82245-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82245-105">Syntax</span></span>

<span data-ttu-id="82245-106">*Catálogo*. Crear*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="82245-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="82245-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82245-107">Parameters</span></span>

  - <span data-ttu-id="82245-108">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="82245-108">*ConnectString*</span></span>

  - <span data-ttu-id="82245-109">Un valor **String** que se utiliza para conectarse al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="82245-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="82245-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82245-110">Remarks</span></span>

<span data-ttu-id="82245-p101">El método **Create** crea y abre una nueva [conexión](connection-object-ado.md) de ADO con el origen de datos especificado en *ConnectString*. Si se ejecuta correctamente, el nuevo objeto **Connection** se asigna a la propiedad [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="82245-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="82245-113">Si el proveedor no admite la creación de catálogos nuevos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="82245-113">An error will occur if the provider does not support creating new catalogs.</span></span>

