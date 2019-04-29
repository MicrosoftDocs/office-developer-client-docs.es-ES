---
title: Constantes (API de disponibilidad)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tema contiene definiciones de constantes, identificadores de clase e identificadores de interfaz para la API de disponibilidad.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431536"
---
# <a name="constants-freebusy-api"></a>Constantes (API de disponibilidad)

Este tema contiene definiciones de constantes, identificadores de clase e identificadores de interfaz para la API de disponibilidad.
  
## <a name="constants"></a>Constantes

|**Constante**|**Definición**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Tal y como se define en el archivo de encabezado Winerror. h del kit de desarrollo de software (SDK) de Microsoft Windows.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Como se define en el archivo de encabezado Winerror. h de Windows SDK.*  <br/> |
|S_FALSE  <br/> | *Como se define en el archivo de encabezado Winerror. h de Windows SDK.*  <br/> |
|S_OK  <br/> | *Como se define en el archivo de encabezado Winerror. h de Windows SDK.*  <br/> |
   
## <a name="interface-identifiers"></a>Identificadores de interfaz

Para los siguientes identificadores de interfaz, asuma la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h del SDK de Windows para asociar el nombre simbólico GUID con su valor.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0X0, 0X0, 0xc0, 0X0, 0X0, 0X0, 0X0, 0X0, 0X0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0X0, 0X0, 0xc0, 0X0, 0X0, 0X0, 0X0, 0X0, 0X0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0X0, 0X0, 0xc0, 0X0, 0X0, 0X0, 0X0, 0X0, 0X0, 0x46);
  

