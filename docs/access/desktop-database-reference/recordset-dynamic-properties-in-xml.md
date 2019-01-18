---
title: Propiedades dinámicas de conjuntos de registros en XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712837"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="c7811-102">Propiedades dinámicas de conjuntos de registros en XML</span><span class="sxs-lookup"><span data-stu-id="c7811-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="c7811-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7811-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7811-104">Las siguientes propiedades de **conjuntos de registros** específicas del proveedor (del Client Cursor Engine) persisten actualmente en el formato XML:</span><span class="sxs-lookup"><span data-stu-id="c7811-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="c7811-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="c7811-105">**AutoRecalc**</span></span>
- <span data-ttu-id="c7811-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="c7811-106">**BatchSize**</span></span>
- <span data-ttu-id="c7811-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="c7811-107">**CommandTimeout**</span></span>
- <span data-ttu-id="c7811-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="c7811-108">**IRowsetChange**</span></span>
- <span data-ttu-id="c7811-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="c7811-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="c7811-110">**Reshape Name**</span><span class="sxs-lookup"><span data-stu-id="c7811-110">**Reshape Name**</span></span>
- <span data-ttu-id="c7811-111">**Resync Command**</span><span class="sxs-lookup"><span data-stu-id="c7811-111">**Resync Command**</span></span>
- <span data-ttu-id="c7811-112">**Unique Catalog**</span><span class="sxs-lookup"><span data-stu-id="c7811-112">**Unique Catalog**</span></span>
- <span data-ttu-id="c7811-113">**Unique Schema**</span><span class="sxs-lookup"><span data-stu-id="c7811-113">**Unique Schema**</span></span>
- <span data-ttu-id="c7811-114">**Unique Table**</span><span class="sxs-lookup"><span data-stu-id="c7811-114">**Unique Table**</span></span>
- <span data-ttu-id="c7811-115">**Update Resync**</span><span class="sxs-lookup"><span data-stu-id="c7811-115">**Update Resync**</span></span>
- <span data-ttu-id="c7811-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="c7811-116">**UpdateCriteria**</span></span>


<span data-ttu-id="c7811-p101">Estas propiedades se guardan en la sección de esquema como atributos de la definición de elemento para el **conjunto de registros** que se hace persistente. Estos atributos se definen en el espacio de nombres de esquema del conjunto de filas y deben tener el prefijo "rs:".</span><span class="sxs-lookup"><span data-stu-id="c7811-p101">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted. These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="c7811-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="c7811-119">See also</span></span>

- [<span data-ttu-id="c7811-120">Propiedades dinámicas de ADO</span><span class="sxs-lookup"><span data-stu-id="c7811-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
