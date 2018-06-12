---
title: Constantes (API de libre/ocupado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tema contiene las definiciones de constantes, los identificadores de clase y los identificadores de interfaz para la API de la información de disponibilidad.
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816063"
---
# <a name="constants-freebusy-api"></a>Constantes (API de libre/ocupado)

Este tema contiene las definiciones de constantes, los identificadores de clase y los identificadores de interfaz para la API de la información de disponibilidad.
  
## <a name="constants"></a>Constantes

|**Constante**|**Definición**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*  <br/> |
|S_FALSE  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*  <br/> |
|S_OK  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*  <br/> |
   
## <a name="interface-identifiers"></a>Identificadores de interfaz

Para los siguientes identificadores de interfaz, se supone la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Windows SDK para asociar el nombre simbólico de GUID a su valor.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46);
  

