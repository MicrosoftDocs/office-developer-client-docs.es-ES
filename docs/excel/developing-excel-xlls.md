---
title: Desarrollo de XLL de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- complementos - [excel 2007], el desarrollo de XLL - [Excel 2007], XLL - [Excel 2007], desarrollo
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815534"
---
# <a name="developing-excel-xlls"></a>Desarrollo de XLL de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La razón principal para escribir los XLL de Microsoft Excel y uso de la API de C es crear funciones de hoja de cálculo de alto rendimiento. Las aplicaciones de funciones de alto rendimiento: y, a partir de Excel 2007, la capacidad de escribir interfaces multiproceso en recursos de servidor eficaces: realizar una parte muy importante de la extensibilidad de Excel. El rendimiento de los XLL estaba más mejorada en Excel 2007 mediante la adición de nuevos tipos de datos y, más importante, compatibilidad con subprocesamiento múltiple.
  
La API C no tiene ninguna de las características de desarrollo rápido de nivel superior de Microsoft Visual Basic para aplicaciones (VBA), COM o Microsoft .NET Framework. Administración de memoria es nivel bajo y por lo tanto, delega mayor responsabilidad en el programador. Muchas características de Excel que se exponen a través de COM, habilitarlos a través de VBA y .NET Framework, no se exponen a la API de C.


- [Conceptos de programación de Excel](excel-programming-concepts.md)
  
- [Trabajar con DLL](working-with-dlls.md)
  
- [Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)
  
- [Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Crear XLL](creating-xlls.md)
  
- [Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Multiproceso y administración de la memoria](multithreading-and-memory-management.md)
  
- [Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)
  
- [Funciones de seguridad de grupo](cluster-safe-functions.md)
  
- [Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)
  
- [Mostrar cuadros de diálogo de un DLL o XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Obtener acceso a la instancia de Excel y los controladores de la ventana principal](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Compatibilidad con versiones anteriores](backward-compatibility.md)
  

