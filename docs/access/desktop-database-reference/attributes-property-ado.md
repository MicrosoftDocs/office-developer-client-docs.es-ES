---
<<<<<<< Título HEAD: atributos (propiedad) (ADO) TOCTitle: atributos (propiedad) (ADO) === título: atributos (propiedad, ADO) TOCTitle: atributos (propiedad, ADO)
>>>>>>> Master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: ms.date 48544716: 18/09/2015 mtps_version: Office.15 f1_keywords:
- ado210.chm1231117 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="attributes-property-ado"></a>Attributes (propiedad, ADO)
=======
# <a name="attributes-property-ado"></a>Attributes (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013


## <a name="attributes-property"></a>Propiedad Attributes

Indica una o varias características de un objeto.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Long**.

Para un objeto [Connection](connection-object-ado.md), la propiedad **Attributes** es de lectura y escritura, y su valor puede ser la suma de uno o varios valores de [XactAttributeEnum](xactattributeenum.md). El valor predeterminado es cero (0).

Para un objeto [Parameter](parameter-object-ado.md), la propiedad **Attributes** es de lectura y escritura, y su valor puede ser la suma de uno o varios valores de [ParameterAttributesEnum](parameterattributesenum.md). El valor predeterminado es **adParamSigned**.

Para un objeto [Field](field-object-ado.md), la propiedad **Attributes** puede ser la suma de uno o varios valores de [FieldAttributeEnum](fieldattributeenum.md). Normalmente, es de sólo lectura. Sin embargo, para los objetos **Field** nuevos que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Attributes** es de lectura y escritura sólo después de especificarse la propiedad [Value](value-property-ado.md) del objeto **Field** y de agregar el proveedor correctamente el nuevo objeto **Field** mediante una llamada al método [Update](update-method-ado.md) de la colección **Fields**.

Para un objeto [Property](property-object-ado.md), la propiedad **Attributes** es de sólo lectura, y su valor puede ser la suma de uno o varios valores de [PropertyAttributesEnum](propertyattributesenum.md).

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Attributes** para establecer o devolver las características de los objetos **Field**, **Property**, [Connection](field-object-ado.md) o [Parameter](property-object-ado.md).

Cuando establece varios atributos, puede sumar las constantes apropiadas. Si establece el valor de la propiedad en una suma que incluye constantes incompatibles, se genera un error.

**Uso de servicio de datos remotos** Esta propiedad no está disponible en un objeto de **conexión** de cliente.

