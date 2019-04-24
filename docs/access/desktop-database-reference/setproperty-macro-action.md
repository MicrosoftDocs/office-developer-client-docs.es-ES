---
title: DefinirPropiedad (acción de macro)
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314577"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="11c24-102">DefinirPropiedad (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="11c24-102">SetProperty macro action</span></span>

<span data-ttu-id="11c24-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11c24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11c24-104">Puede usar la acción **DefinirPropiedad** para definir una propiedad de un control ubicado en un formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="11c24-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="11c24-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="11c24-105">Setting</span></span>

<span data-ttu-id="11c24-106">La acción **DefinirPropiedad** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="11c24-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11c24-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="11c24-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="11c24-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="11c24-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11c24-109">Nombre del control</span><span class="sxs-lookup"><span data-stu-id="11c24-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="11c24-p101">Escriba el nombre del campo o control para el cual desee definir el valor de una propiedad. Use sólo el nombre del control en vez de la sintaxis completa. Deje este argumento en blanco para definir la propiedad del actual formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="11c24-p101">Type the name of the field or control for which you want to set the property value. Use only the control name, not the full syntax. Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11c24-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11c24-113">Property</span></span></p></td>
<td><p><span data-ttu-id="11c24-p102">Seleccione la propiedad que desee definir. Vea la sección <strong>Comentarios</strong> de este artículo para ver una lista de las propiedades que se pueden definir mediante esta acción.</span><span class="sxs-lookup"><span data-stu-id="11c24-p102">Select the property that you want to set. See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11c24-116">Valor</span><span class="sxs-lookup"><span data-stu-id="11c24-116">Value</span></span></p></td>
<td><p><span data-ttu-id="11c24-p103">Escriba el valor en el que desee establecer la propiedad. Para las propiedades cuyos valores son Sí o No, use <strong>-1</strong> para Sí y <strong>0</strong> para No.</span><span class="sxs-lookup"><span data-stu-id="11c24-p103">Type the value that the property is to be set to. For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="11c24-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11c24-119">Remarks</span></span>

- <span data-ttu-id="11c24-120">Puede usar la acción **DefinirPropiedad** para definir las siguientes propiedades de un control: **Habilitada**, **Visible**, **Bloqueada**, **Izquierda**, **Superior**, **Ancho**, **Alto**, **Color de primer plano**, **Color de fondo** y **Título**.</span><span class="sxs-lookup"><span data-stu-id="11c24-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="11c24-121">Si especifica un valor no válido para el argumento ***Valor***, no se genera ningún error, pero puede que Access cambie el valor de la propiedad según su interpretación del argumento.</span><span class="sxs-lookup"><span data-stu-id="11c24-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="11c24-p104">Puede usar la acción **DefinirPropiedad** en una macro independiente sólo si va precedida de una acción que seleccione el formulario o informe que contiene el control cuya propiedad va a establecer. Si el formulario o informe no está abierto, puede usar la acción **AbrirFormulario** o **AbrirInforme** para abrirlo y seleccionarlo. Si el formulario o informe ya está abierto, puede usar la acción **SeleccionarObjeto** para seleccionarlo. A continuación, puede usar la acción **DefinirPropiedad** para definir la propiedad. No es necesario que seleccione el objeto si usa la acción **DefinirPropiedad** en una macro incrustada en un control ubicado en el mismo formulario o informe que el control cuya propiedad va a definir.</span><span class="sxs-lookup"><span data-stu-id="11c24-p104">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="11c24-127">Para ejecutar la acción **DefinirPropiedad** en un módulo de VBA, use el método **SetProperty** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="11c24-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="11c24-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11c24-128">Example</span></span>

<span data-ttu-id="11c24-129">El siguiente ejemplo muestra cómo usar la acción SetProperty para alternar la visibilidad del cuadro de texto **MiCuadroDeTexto**.</span><span class="sxs-lookup"><span data-stu-id="11c24-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="11c24-130">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="11c24-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
