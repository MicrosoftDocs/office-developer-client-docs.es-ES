---
title: Obtener acceso a código XLL en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- obtener acceso al código xll [excel 2007], XLL [Excel 2007], obtener acceso a código, comandos [Excel 2007], registro, funciones [Excel 2007], registro llamadas a XLL desde Excel, registrar comandos [Excel 2007], registrar funciones [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304189"
---
# <a name="accessing-xll-code-in-excel"></a>Obtener acceso a código XLL en Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para que sean accesibles en Microsoft Excel, las funciones y los comandos que contiene un XLL:
  
- Las debe exportar el XLL.
    
- Deben estar registradas con Excel.
    
## <a name="registering-functions-and-commands-with-excel"></a>Registrar las funciones y comandos con Excel

El registro indica a Excel lo siguiente sobre un punto de entrada de la DLL:
  
- Si está oculto o, si es una función, si está visible en el Asistente para funciones.
    
- Si se puede llamar solo desde una hoja de macros XLM o también desde una hoja de cálculo.
    
- Si es un comando, si es una función de hoja de cálculo o una función equivalente de hoja de macros.
    
- Cuál es el nombre de la exportación DLL o XLL y qué nombre desea que use Excel.
    
- Si es una función:
    
  - Qué tipos de datos devuelve y toma como argumentos.
    
  - Si devuelve el resultado modificando un argumento en su lugar.
    
  - Si es volátil.
    
  - Si es seguro para subprocesos (compatible a partir de Excel 2007).
    
  - Qué texto deben mostrar el Asistente para funciones de pegado y el editor de Autocompletar para ayudar con la función de llamadas.
    
  - La categoría de la función en la que se debe enumerar.
    
Todo ello se consigue con la función de la API de C [xlfRegister](xlfregister-form-1.md), equivalente a la función XLM **REGISTER**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Llamadas a funciones XLL directamente desde Excel

Una vez que se han registrado, se puede llamar a las funciones de hoja de macros y la hoja de cálculo XLL desde cualquier lugar donde se pueda llamar a una función integrada:
  
- Una fórmula de matriz o de celda en una hoja de cálculo.
    
- Una fórmula de matriz o de celda en una hoja de macros.
    
- La definición de un nombre definido.
    
- Los campos de condición y de límite de un cuadro de diálogo con formato condicional.
    
- Desde otro complemento a través de la función de la API de C [xlUDF](xludf.md).
    
- Desde Visual Basic para aplicaciones (VBA) a través del método **Application.Run**. 
    
Puede obtener una referencia a la celda o rango de celdas de llamada dentro de su función con la función de la API de C **xlfCaller**. Si se llama a la función desde la expresión de formato condicional de la celda, se sigue devolviendo una referencia a la celda o celdas asociadas, por lo que no puede suponer que la fórmula contiene la función XLL. Si la función se invoca desde una función VBA definida por el usuario (UDF), **xlfCaller** devuelve de nuevo a la dirección de las celdas que llamaron a la función VBA. Para obtener más información, vea [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel también llama al código de la función XLL de la **Asistente para funciones de pegado** y los cuadros de diálogo **Reemplazar**. Es posible que deba restringir la ejecución habitual del código en el caso del cuadro de diálogo **Argumentos para funciones de pegado** especialmente cuando la función puede tardar mucho tiempo en ejecutarse. Para detectar si se llama a la función desde uno de estos cuadros de diálogo, deberá implementar en su proyecto código que recorra todas las ventanas abiertas para determinar si la ventana frontal es uno de estos cuadros de diálogo y, si es así, cuál. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Llamar a los comandos XLL directamente desde Excel

Una vez que se han registrado, se puede llamar a los comandos XLL de las mismas formas que se puede llamar a otras macros definidas por el usuario:
  
- Si se asocia a un objeto de control incrustado en una hoja de cálculo.
    
- Desde el cuadro de diálogo Ejecutar macro.
    
- Desde una macro VBA definida por el usuario con el método **Application.Run**. 
    
- Desde un elemento de menú o barra de herramientas personalizados.
    
- Con una pulsación de tecla de método abreviado configurada cuando se registra el comando.
    
- Como el comando que se ejecuta cuando se captura un evento específico.
    
> [!NOTE]
> Los comandos XLL están ocultos, pues no aparecen en la lista de macros disponibles en los cuadros de diálogo de Excel. Pero se pueden especificar manualmente en el campo de nombre de la macro. Excel espera el nombre "registrado como" en estos cuadros de diálogo, no el nombre de la exportación DLL. 
  
Excel asume que todos los comandos XLL registrados con Excel tienen el siguiente formato:
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

Excel omite el valor devuelto a menos que se le llame desde una hoja de macros XLM, en cuyo caso el valor devuelto se convierte a **TRUE** o **FALSE**. Por lo tanto, debe devolver 1 si el comando se ejecuta correctamente y 0 si tiene errores o el usuario lo cancela.
  
Puede obtener información sobre cómo se invocó el comando utilizando la función de la API de C **xlfCaller**. Para obtener más información, vea [xlfCaller](xlfcaller.md).
  
A partir de Excel 2007, la interfaz de usuario es muy diferente a la de las versiones anteriores. Las funciones de la API de C que permiten la adición y eliminación de barras de menús, menús, submenús, elementos de menú, barras de herramientas personalizadas y botones de la barra de herramientas aún son compatibles en la mayoría de los casos. No obstante, puede que no siempre hagan el elemento agregado disponible de un modo que resulte familiar a los usuarios. Compruebe con cuidado que las funciones agregadas sigan siendo accesibles o implemente una personalización específica de la versión. Empezando en Excel 2007, la interfaz de usuario se personaliza mejor a través de un módulo de código administrado que puede trabajar estrechamente con los comandos XLL.
  
## <a name="see-also"></a>Vea también

- [Crear XLL](creating-xlls.md)
- [Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)
- [Desarrollo de XLL de Excel](developing-excel-xlls.md)



