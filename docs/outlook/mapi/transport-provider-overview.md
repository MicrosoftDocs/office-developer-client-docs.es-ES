---
title: Información general sobre el proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820897"
---
# <a name="transport-provider-overview"></a>Información general sobre el proveedor de transporte

  
  
**Se aplica a**: Outlook 
  
Un proveedor de transporte es una biblioteca de vínculos dinámicos (DLL) que actúa como intermediario entre el subsistema MAPI y uno o varios sistemas de mensajería subyacentes. Un sistema de mensajería es algunos mecanismo específico mediante el cual se envían y reciben los mensajes. Algunos ejemplos de sistemas de mensajería son:
  
- Un sistema de archivos de red compartida que el proveedor de transporte escribe los mensajes a directamente.
    
- Una interfaz de red TCP/IP que usa el proveedor de transporte para conectarse a un servidor de mensajería.
    
- Un servicio en línea que los usuarios se conectan a.
    
- Un host sistema basado en mensajería o office automatización.
    
- Un conjunto de llamadas a procedimiento remoto a un servidor de mensajería.
    
- Cualquier cosa que se puede usar para transferir datos desde un equipo a otro.
    
Una DLL del proveedor de transporte debe cumplir con la interfaz especificada por MAPI. Como desarrollador de proveedor de transporte, se implementará esta interfaz en cuanto a la funcionalidad presente en el sistema de mensajería.
  

