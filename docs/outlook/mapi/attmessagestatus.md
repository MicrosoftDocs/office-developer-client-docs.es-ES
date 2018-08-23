---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565749"
---
# <a name="attmessagestatus"></a><span data-ttu-id="82712-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="82712-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="82712-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82712-105">Indicadores de mensaje MAPI se asignan a marcas TNEF para preservar la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="82712-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="82712-106">Todos los indicadores se agrupan juntos y codificados en un solo byte.</span><span class="sxs-lookup"><span data-stu-id="82712-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="82712-107">Las asignaciones son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="82712-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="82712-108">**Indicadores de mensaje MAPI**</span><span class="sxs-lookup"><span data-stu-id="82712-108">**MAPI message flags**</span></span>|<span data-ttu-id="82712-109">**Indicadores TNEF**</span><span class="sxs-lookup"><span data-stu-id="82712-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82712-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="82712-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="82712-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="82712-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="82712-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="82712-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="82712-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="82712-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="82712-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="82712-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="82712-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="82712-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="82712-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="82712-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="82712-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="82712-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="82712-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="82712-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="82712-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="82712-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="82712-120">Estos marcadores se definen en el TNEF. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="82712-120">These flags are defined in the TNEF.H header file.</span></span>
  

