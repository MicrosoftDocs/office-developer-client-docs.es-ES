---
title: Introducción a los proveedores de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356640"
---
# <a name="transport-provider-overview"></a>Introducción a los proveedores de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de transporte es una biblioteca de vínculos dinámicos (DLL) que actúa como intermediario entre el subsistema MAPI y uno o varios sistemas de mensajería subyacentes. Un sistema de mensajería es un mecanismo específico por el que se envían y reciben los mensajes. Algunos ejemplos de sistemas de mensajería son:
  
- Un sistema de archivos de red compartido en el que el proveedor de transporte escribe mensajes directamente.
    
- Una interfaz de red TCP/IP que el proveedor de transporte usa para conectarse a un servidor de mensajería.
    
- Un servicio en línea al que se conectan los usuarios.
    
- Un sistema de mensajería basada en host o de automatización de Office.
    
- Un conjunto de llamadas a procedimientos remotos a un servidor de mensajería.
    
- Todo lo que se puede usar para transferir datos de un equipo a otro.
    
Un proveedor de transporte DLL debe cumplir con la interfaz especificada por MAPI. Como desarrollador de un proveedor de transporte, implementará esta interfaz en función de la funcionalidad presente en el sistema de mensajería.
  

