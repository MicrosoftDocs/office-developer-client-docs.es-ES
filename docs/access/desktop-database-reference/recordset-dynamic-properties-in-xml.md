---
title: Propiedades dinámicas de conjuntos de registros en XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483665"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="bc9f5-102">Propiedades dinámicas de conjuntos de registros en XML</span><span class="sxs-lookup"><span data-stu-id="bc9f5-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="bc9f5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc9f5-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="bc9f5-104">Propiedades dinámicas de conjuntos de registros en XML</span><span class="sxs-lookup"><span data-stu-id="bc9f5-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="bc9f5-105">Las siguientes propiedades de **conjuntos de registros** específicas del proveedor (del Client Cursor Engine) persisten actualmente en el formato XML:</span><span class="sxs-lookup"><span data-stu-id="bc9f5-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="bc9f5-106">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-106">**Update Resync**</span></span>

  - <span data-ttu-id="bc9f5-107">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-107">**Unique Table**</span></span>

  - <span data-ttu-id="bc9f5-108">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-108">**Unique Schema**</span></span>

  - <span data-ttu-id="bc9f5-109">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="bc9f5-110">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-110">**Resync Command**</span></span>

  - <span data-ttu-id="bc9f5-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="bc9f5-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="bc9f5-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="bc9f5-114">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-114">**BatchSize**</span></span>

  - <span data-ttu-id="bc9f5-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="bc9f5-116">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-116">**Reshape Name**</span></span>

  - <span data-ttu-id="bc9f5-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="bc9f5-117">**AutoRecalc**</span></span>

<span data-ttu-id="bc9f5-p101">Estas propiedades se guardan en la sección de esquema como atributos de la definición de elemento para el **conjunto de registros** que se hace persistente. Estos atributos se definen en el espacio de nombres de esquema del conjunto de filas y deben tener el prefijo "rs:".</span><span class="sxs-lookup"><span data-stu-id="bc9f5-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

