---
title: Introducción al proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433160"
---
# <a name="transport-provider-overview"></a>Introducción al proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de transporte es una biblioteca de vínculos dinámicos (DLL) que actúa como intermediario entre el subsistema MAPI y uno o más sistemas de mensajería subyacentes. Un sistema de mensajería es un mecanismo específico mediante el cual se envían y reciben mensajes. Algunos ejemplos de sistemas de mensajería son:
  
- Un sistema de archivos de red compartido en el que el proveedor de transporte escribe mensajes directamente.
    
- Una interfaz de red TCP/IP que el proveedor de transporte usa para conectarse a un servidor de mensajería.
    
- Un servicio en línea al que se conectan los usuarios.
    
- Un sistema de automatización de office o mensajería basado en host.
    
- Conjunto de llamadas de procedimiento remoto a un servidor de mensajería.
    
- Cualquier cosa que se pueda usar para transferir datos de un equipo a otro.
    
Una DLL del proveedor de transporte debe cumplir con la interfaz especificada por MAPI. Como desarrollador del proveedor de transporte, implementará esta interfaz en términos de la funcionalidad presente en el sistema de mensajería.
  

