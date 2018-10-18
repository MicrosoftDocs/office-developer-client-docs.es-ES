---
título: ocultar la cinta de opciones al iniciar Access TOCTitle: ocultar la cinta de opciones al iniciar Access <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 18/09/2015 === Descripción: cómo cargar una cinta de opciones personalizada que oculte todas las fichas integradas en Access 2013.
MS:AssetId: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 16/10/2018
>>>>>>> mtps_version principal: Office.15
---

# <a name="hide-the-ribbon-when-access-starts"></a>Ocultar la cinta de opciones al iniciar Access

**Se aplica a:** Access 2013 | Office 2013

De manera predeterminada, Microsoft Access no dispone de un método para ocultar la cinta. En este tema se describe de qué manera se puede cargar una cinta personalizada que oculte todas las fichas integradas.

Para cargar la Cinta de opciones personalizada al iniciar Access, deberá almacenar su configuración en una tabla denominada **USysRibbons**.

<<<<<<< Encabezado de la tabla **USysRibbons** debe crearse utilizando nombres de columna específicos en orden para las personalizaciones de la cinta de opciones para se puedan implementar. La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.
=== La tabla **USysRibbons** debe crearse utilizando nombres de columna específicos para las personalizaciones de la cinta de opciones para se puedan implementar. 

La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.
>>>>>>> master

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<<<<<<< HEAD
<th><p>Nombre de columna</p></th>
<th><p>Tipo de datos</p></th>
=======
<th><p>Nombre de columna</p></th>
<th><p>Tipo de datos</p></th>
>>>>>>>patrón
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Texto</p></td>
<td><p>Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memo</p></td>
<<<<<<< HEAD
<td><p>Contiene el código XML de extensibilidad de la Cinta de opciones (RibbonX) que define la personalización de la Cinta de opciones.</p></td>
=======
<td><p>Contiene el XML (RibbonX) que define la personalización de la cinta de opciones de extensibilidad de la cinta de opciones.</p></td>
>>>>>>>patrón
</tr>
</tbody>
</table>

<<<<<<< HEAD

La tabla siguiente describe los valores de personalización de la Cinta de opciones que se deben almacenar en la tabla **USysRibbons**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de columna</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>HideTheRibbon</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;la cinta de opciones startFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a>Aplicar la Cinta de opciones personalizada al iniciar Access
=======
<br/>

La tabla siguiente describe los valores de personalización de la Cinta de opciones que se deben almacenar en la tabla **USysRibbons**.

|Nombre de columna|Valor|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Aplicar una cinta de opciones personalizada al iniciar Access
>>>>>>> master

Para implementar una interfaz de usuario personalizada con objeto de que esté disponible al iniciarse la aplicación, haga lo siguiente:

1.  Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.

2.  Cierre la aplicación y, a continuación, reiníciela.

<<<<<<< HEAD
3.  Haga clic en el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y, a continuación, haga clic en **Opciones de Access**.

4.  Haga clic en la opción **Base de datos activa** y, a continuación, en la sección **Opciones de barra de herramientas y de la cinta de opciones**, haga clic en la lista **Nombre de cinta de opciones** y seleccione **HideTheRibbon**.
=======
3.  Elija el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")y, a continuación, elija **Opciones de Access**.

4.  Elija la opción de **Base de datos actual** y, a continuación, en la sección **Opciones de barra de herramientas y la cinta de opciones** , elija la lista **Nombre de la cinta de opciones** y seleccione **HideTheRibbon**.
>>>>>>> master

5.  Cierre y vuelva a iniciar la aplicación.

> [!NOTE]
> [!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


