---
<<<<<<< Título HEAD: ParentURL (propiedad) (ADO) TOCTitle: ParentURL (propiedad) (ADO) === título: ParentURL (propiedad, ADO) TOCTitle: ParentURL (propiedad, ADO)
>>>>>>> Master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: ms.date 48548517: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="parenturl-property-ado"></a>ParentURL (propiedad, ADO)
=======
# <a name="parenturl-property-ado"></a>ParentURL (propiedad, ADO)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Indica una cadena URL absoluta que apunta al objeto [Record](record-object-ado.md) primario del objeto **Record** actual.

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **String** que indica la dirección URL del objeto **Record** primario.

## <a name="remarks"></a>Comentarios

La propiedad **ParentURL** depende del origen usado para abrir el objeto **Record**. Por ejemplo, **Record** se puede abrir mediante un origen que contenga el nombre de ruta de acceso relativa de un directorio al que se hace referencia por medio de la propiedad [ActiveConnection](activeconnection-property-ado.md).

Imagine que "second" es una carpeta incluida en "first". Abra el objeto **Record** mediante el siguiente código:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Ahora, el valor de la propiedad **ParentURL** es la propiedad **ParentURL** es "https://first", al igual que **ActiveConnection**.

El origen también puede ser una dirección URL absoluta, como "https://first/second". La propiedad **ParentURL** es "https://first", el nivel superior. La propiedad **ParentURL** es "https://first", el nivel superior "segundo".

Esta propiedad puede ser un valor nulo si:

- No hay ningún elemento primario para el objeto actual; por ejemplo, si el objeto **Record** representa la raíz de un directorio.

- El objeto **Record** representa una entidad que no se puede especificar con una dirección URL.

Esta propiedad es de sólo lectura.


> [!NOTE]
> - [!NOTA] Esta propiedad sólo es admitida por proveedores de origen de documentos, como el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Registros y campos proporcionados por un proveedor](records-and-provider-supplied-fields.md).
> - [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente Microsoft OLE DB Provider for Internet Publishing. Para obtener más información, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md). 
> - [!NOTA] Si el registro actual incluye un registro de datos de un objeto **Recordset** ADO, el acceso a la propiedad **ParentURL** provoca un error en tiempo de ejecución, lo que indica que no hay dirección URL posible.


