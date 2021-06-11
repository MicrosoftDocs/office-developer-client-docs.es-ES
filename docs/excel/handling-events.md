---
title: Controlar eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438270"
---
# <a name="handling-events"></a>Controlar eventos

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
A partir Excel 2010, los XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica. Los eventos son los siguientes:
  
- **CalculationEnded:** se genera cuando Excel termina de calcular. Después de este evento, puede liberar los recursos asignados durante el cálculo.
    
- **CalculationCanceled:** se genera cuando el usuario interrumpe el cálculo. El XLL detiene cualquier actividad asincrónica. Inmediatamente después de este evento, se genera el **evento CalculationEnded.** 
    
Para controlar estos eventos, XLL usa la función de API de C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** y **CalculationCanceled** no se genera durante el recálculo mediante programación. 
  

