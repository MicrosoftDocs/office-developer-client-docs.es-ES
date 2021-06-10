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
# <a name="setproperty-macro-action"></a>DefinirPropiedad (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **DefinirPropiedad** para definir una propiedad de un control ubicado en un formulario o informe.

## <a name="setting"></a>Configuración

La acción **DefinirPropiedad** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nombre del control</p></td>
<td><p>Escriba el nombre del campo o control para el cual desee definir el valor de una propiedad. Use sólo el nombre del control en vez de la sintaxis completa. Deje este argumento en blanco para definir la propiedad del actual formulario o informe.</p></td>
</tr>
<tr class="even">
<td><p>Propiedad</p></td>
<td><p>Seleccione la propiedad que desee definir. Vea la sección <strong>Comentarios</strong> de este artículo para ver una lista de las propiedades que se pueden definir mediante esta acción.</p></td>
</tr>
<tr class="odd">
<td><p>Valor</p></td>
<td><p>Escriba el valor en el que desee establecer la propiedad. Para las propiedades cuyos valores son Sí o No, use <strong>-1</strong> para Sí y <strong>0</strong> para No.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

- Puede usar la acción **DefinirPropiedad** para definir las siguientes propiedades de un control: **Habilitada**, **Visible**, **Bloqueada**, **Izquierda**, **Superior**, **Ancho**, **Alto**, **Color de primer plano**, **Color de fondo** y **Título**.

- Si especifica un valor no válido para el argumento ***Valor***, no se genera ningún error, pero puede que Access cambie el valor de la propiedad según su interpretación del argumento.

- Puede usar la acción **DefinirPropiedad** en una macro independiente sólo si va precedida de una acción que seleccione el formulario o informe que contiene el control cuya propiedad va a establecer. Si el formulario o informe no está abierto, puede usar la acción **AbrirFormulario** o **AbrirInforme** para abrirlo y seleccionarlo. Si el formulario o informe ya está abierto, puede usar la acción **SeleccionarObjeto** para seleccionarlo. A continuación, puede usar la acción **DefinirPropiedad** para definir la propiedad. No es necesario que seleccione el objeto si usa la acción **DefinirPropiedad** en una macro incrustada en un control ubicado en el mismo formulario o informe que el control cuya propiedad va a definir.

- Para ejecutar la acción **DefinirPropiedad** en un módulo de VBA, use el método **SetProperty** del objeto **DoCmd**.

## <a name="example"></a>Ejemplo

El siguiente ejemplo muestra cómo usar la acción SetProperty para alternar la visibilidad del cuadro de texto **MiCuadroDeTexto**.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
