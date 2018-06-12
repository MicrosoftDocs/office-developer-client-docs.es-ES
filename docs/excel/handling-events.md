---
title: Controlar eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815631"
---
# <a name="handling-events"></a>Controlar eventos

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Iniciar en Excel 2010, XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica. Los eventos son los siguientes:
  
- **CalculationEnded**: se produce cuando finalice Excel calcular. Después de este evento, puede liberar recursos asignados durante el cálculo.
    
- **CalculationCanceled**: se produce cuando el usuario los cálculos interrumpe el cálculo. El XLL detiene cualquier actividades asincrónicas. Inmediatamente después de este evento se desencadena el evento **CalculationEnded** . 
    
Para controlar estos eventos, el XLL usa la función de API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** y **CalculationCanceled** no se ha generado durante la actualización mediante programación. 
  

