---
title: Conectar (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295985"
---
# <a name="connect-property-rds"></a><span data-ttu-id="a57ad-102">Conectar (RDS)</span><span class="sxs-lookup"><span data-stu-id="a57ad-102">Connect property (RDS)</span></span>

<span data-ttu-id="a57ad-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a57ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a57ad-104">Indica el nombre de la base de datos desde la que se ejecutan las operaciones de consulta y actualización.</span><span class="sxs-lookup"><span data-stu-id="a57ad-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="a57ad-105">La propiedad **Connect** se puede establecer en tiempo de diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md), o bien en tiempo de ejecución en el código del scripting (por ejemplo, VBScript).</span><span class="sxs-lookup"><span data-stu-id="a57ad-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="a57ad-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a57ad-106">Syntax</span></span>

<span data-ttu-id="a57ad-107">Tiempo de diseño: \< PARAM NAME="Conectar" VALUE="ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="a57ad-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="a57ad-108">Tiempo de ejecución: DataControl. Conectar = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="a57ad-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="a57ad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a57ad-109">Parameters</span></span>

|<span data-ttu-id="a57ad-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a57ad-110">Parameter</span></span>|<span data-ttu-id="a57ad-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a57ad-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a57ad-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="a57ad-112">*ConnectionString*</span></span> |<span data-ttu-id="a57ad-p101">Cadena de conexión válida. Para obtener información más general sobre las cadenas de conexión, vea la propiedad [ConnectionString](connectionstring-property-ado.md) o vea la documentación de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="a57ad-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="a57ad-115">**NOTA:** Especificación de MS Remote como proveedor de **RDS. DataControl** crearía un escenario de cuatro niveles.</span><span class="sxs-lookup"><span data-stu-id="a57ad-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="a57ad-116">No se han probado los escenarios de más de tres niveles y, en principio, no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="a57ad-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="a57ad-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="a57ad-117">*DataControl*</span></span> |<span data-ttu-id="a57ad-118">Variable de objeto que representa un objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="a57ad-118">An object variable that represents an **RDS.DataControl** object.</span></span>|

