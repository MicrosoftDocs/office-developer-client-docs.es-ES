---
title: atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408281"
---
# <a name="attdate-attributes"></a><span data-ttu-id="4ba0f-103">atributos attDate</span><span class="sxs-lookup"><span data-stu-id="4ba0f-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="4ba0f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ba0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ba0f-105">Todas las propiedades MAPI relacionadas con fechas y horas se asignan a atributos TNEF que tienen el **prefijo attDate.**</span><span class="sxs-lookup"><span data-stu-id="4ba0f-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="4ba0f-106">Todas se codifican como **estructuras DTR.**</span><span class="sxs-lookup"><span data-stu-id="4ba0f-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="4ba0f-107">Las fechas y horas de los atributos de datos adjuntos también se codifican como **estructuras DTR.**</span><span class="sxs-lookup"><span data-stu-id="4ba0f-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="4ba0f-108">Todas las propiedades MAPI relacionadas con fechas y horas se asignan a atributos TNEF que tienen el **prefijo attDate.**</span><span class="sxs-lookup"><span data-stu-id="4ba0f-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="4ba0f-109">Todas se codifican como **estructuras DTR.**</span><span class="sxs-lookup"><span data-stu-id="4ba0f-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="4ba0f-110">Las fechas y horas de los atributos de datos adjuntos también se codifican como **estructuras DTR.**</span><span class="sxs-lookup"><span data-stu-id="4ba0f-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="4ba0f-111">Una **estructura DTR** es muy similar a la **estructura SYSTEMTIME** definida en los archivos de encabezado win32.</span><span class="sxs-lookup"><span data-stu-id="4ba0f-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="4ba0f-112">La **estructura DTR** se codifica en la secuencia TNEF como bytes **sizeof(DTR)** empezando por el primer miembro de la estructura.</span><span class="sxs-lookup"><span data-stu-id="4ba0f-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="4ba0f-113">La **estructura dtr** se define en el TNEF. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="4ba0f-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

