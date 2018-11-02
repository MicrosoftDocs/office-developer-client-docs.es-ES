---
title: Create (método, ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01f45adaf5bdd15841be86bfea62cca58e21a9d9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925522"
---
# <a name="create-method-adox"></a><span data-ttu-id="bc7a2-102">Create (método, ADOX)</span><span class="sxs-lookup"><span data-stu-id="bc7a2-102">Create method (ADOX)</span></span>


<span data-ttu-id="bc7a2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc7a2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bc7a2-104">Crea un nuevo catálogo.</span><span class="sxs-lookup"><span data-stu-id="bc7a2-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc7a2-105">Syntax</span></span>

<span data-ttu-id="bc7a2-106">*Catálogo*. Crear*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="bc7a2-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="bc7a2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc7a2-107">Parameters</span></span>

  - <span data-ttu-id="bc7a2-108">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="bc7a2-108">*ConnectString*</span></span>

  - <span data-ttu-id="bc7a2-109">Un valor **String** que se utiliza para conectarse al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="bc7a2-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc7a2-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc7a2-110">Remarks</span></span>

<span data-ttu-id="bc7a2-p101">El método **Create** crea y abre una nueva [conexión](connection-object-ado.md) de ADO con el origen de datos especificado en *ConnectString*. Si se ejecuta correctamente, el nuevo objeto **Connection** se asigna a la propiedad [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="bc7a2-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="bc7a2-113">Si el proveedor no admite la creación de catálogos nuevos, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="bc7a2-113">An error will occur if the provider does not support creating new catalogs.</span></span>

