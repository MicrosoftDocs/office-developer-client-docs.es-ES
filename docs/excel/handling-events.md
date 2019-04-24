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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304042"
---
# <a name="handling-events"></a>Controlar eventos

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
A partir de Excel 2010, los XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica. Los eventos son los siguientes:
  
- **CalculationEnded**: se produce cuando Excel finaliza el cálculo. Después de este evento, puede liberar los recursos asignados durante el cálculo.
    
- **CalculationCanceled**: se produce cuando el usuario interrumpe el cálculo. El XLL detiene todas las actividades asincrónicas. Inmediatamente después de este evento, se genera el evento **CalculationEnded** . 
    
Para controlar estos eventos, el XLL usa la función de la API de C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** y **CalculationCanceled** no se generan durante la actualización mediante programación. 
  

